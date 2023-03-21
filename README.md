# laravel  ReCaptcha Rule

### Validating using FormRequest

```php
use Illuminate\Foundation\Http\FormRequest;
use App\Rules\ReCaptcha;

class TicketRequest extends FormRequest
{
    /**
     * Get the validation rules that apply to the request.
     * @return array
     */
    public function rules()
    {
        return [
            'g-recaptcha-response' => [new ReCaptcha($this->ip())],
        ];
    }
}
```
