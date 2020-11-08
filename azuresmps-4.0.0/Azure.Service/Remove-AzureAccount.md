---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075870"
---
# <span data-ttu-id="85280-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="85280-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="85280-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85280-102">SYNOPSIS</span></span>
<span data-ttu-id="85280-103">Удаление учетной записи Azure из Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85280-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="85280-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85280-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85280-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85280-105">DESCRIPTION</span></span>
<span data-ttu-id="85280-106">Командлет **Remove-AzureAccount** удаляет учетную запись Azure и ее подписки из файла данных подписки в перемещаемом профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="85280-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="85280-107">Эта учетная запись не удаляется из Microsoft Azure, а сама учетная запись может быть изменена любым способом.</span><span class="sxs-lookup"><span data-stu-id="85280-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="85280-108">Использование этого командлета очень похоже на выход из учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="85280-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="85280-109">Кроме того, если вы хотите снова войти в учетную запись, используйте **Add-AzureAccount** или **Import-AzurePublishSettingsFile** , чтобы снова добавить учетную запись в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85280-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="85280-110">Вы также можете использовать командлет **Remove-AzureAccount** , чтобы изменить способ входа командлетов PowerShell для Azure в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="85280-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="85280-111">Если у вашей учетной записи есть сертификат управления из **Import-AzurePublishSettingsFile** и маркер доступа из **Add-AzureAccount** , командлеты PowerShell для Azure используют только маркер доступа. они игнорируют сертификат управления.</span><span class="sxs-lookup"><span data-stu-id="85280-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="85280-112">Чтобы использовать сертификат управления, выполните **Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="85280-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="85280-113">Когда **Remove-AzureAccount** находит как сертификат управления, так и маркер доступа, он удаляет только маркер доступа, а не удаляет учетную запись.</span><span class="sxs-lookup"><span data-stu-id="85280-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="85280-114">Сертификат управления по-прежнему есть, поэтому учетная запись по-прежнему доступна для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85280-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="85280-115">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85280-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="85280-116">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="85280-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="85280-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85280-117">EXAMPLES</span></span>

### <span data-ttu-id="85280-118">Пример 1: Удаление учетной записи</span><span class="sxs-lookup"><span data-stu-id="85280-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="85280-119">Эта команда удаляет admin@contoso.com из файла данных подписки.</span><span class="sxs-lookup"><span data-stu-id="85280-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="85280-120">После завершения команды учетная запись больше не доступна для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85280-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="85280-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85280-121">PARAMETERS</span></span>

### <span data-ttu-id="85280-122">-Force</span><span class="sxs-lookup"><span data-stu-id="85280-122">-Force</span></span>
<span data-ttu-id="85280-123">Подавляет вывод запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="85280-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="85280-124">По умолчанию **Remove-AzureAccount** предложит вам перед удалением учетной записи из Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85280-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85280-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="85280-125">-Name</span></span>
<span data-ttu-id="85280-126">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="85280-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="85280-127">Значение параметра задается с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="85280-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="85280-128">Подстановочные знаки не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="85280-128">Wildcard characters are not supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85280-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85280-129">-PassThru</span></span>
<span data-ttu-id="85280-130">Возвращает $True, если команда выполнена успешно, и $False в случае ее сбоя.</span><span class="sxs-lookup"><span data-stu-id="85280-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="85280-131">По умолчанию этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85280-131">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85280-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="85280-132">-Profile</span></span>
<span data-ttu-id="85280-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="85280-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="85280-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85280-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85280-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85280-135">-Confirm</span></span>
<span data-ttu-id="85280-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85280-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85280-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85280-137">-WhatIf</span></span>
<span data-ttu-id="85280-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85280-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85280-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85280-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85280-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85280-140">CommonParameters</span></span>
<span data-ttu-id="85280-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85280-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85280-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85280-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85280-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85280-143">INPUTS</span></span>

### <span data-ttu-id="85280-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="85280-144">None</span></span>
<span data-ttu-id="85280-145">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="85280-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="85280-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85280-146">OUTPUTS</span></span>

### <span data-ttu-id="85280-147">None и System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85280-147">None or System.Boolean</span></span>
<span data-ttu-id="85280-148">Если вы используете параметр *PassThru* , этот командлет возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="85280-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="85280-149">В противном случае он не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85280-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="85280-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="85280-150">NOTES</span></span>

## <span data-ttu-id="85280-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85280-151">RELATED LINKS</span></span>

[<span data-ttu-id="85280-152">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="85280-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="85280-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="85280-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


