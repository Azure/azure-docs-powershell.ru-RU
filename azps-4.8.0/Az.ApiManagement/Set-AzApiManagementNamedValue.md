---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementNamedValue.md
ms.openlocfilehash: d3902a085ae870034bbb0fbc668d55166b7fe61c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078529"
---
# <span data-ttu-id="da58d-101">Set-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="da58d-101">Set-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="da58d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da58d-102">SYNOPSIS</span></span>
<span data-ttu-id="da58d-103">Изменяет именованное значение для управления API.</span><span class="sxs-lookup"><span data-stu-id="da58d-103">Modifies an API Management Named Value.</span></span>

## <span data-ttu-id="da58d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da58d-104">SYNTAX</span></span>

```
Set-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da58d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da58d-105">DESCRIPTION</span></span>
<span data-ttu-id="da58d-106">Командлет **Set-AzApiManagementNamedValue** изменяет именованное значение управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="da58d-106">The **Set-AzApiManagementNamedValue** cmdlet modifies an Azure API Management Named Value.</span></span>

## <span data-ttu-id="da58d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da58d-107">EXAMPLES</span></span>

### <span data-ttu-id="da58d-108">Пример 1: изменение тегов для именованного значения</span><span class="sxs-lookup"><span data-stu-id="da58d-108">Example 1: Change the tags on the named value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="da58d-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="da58d-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="da58d-110">Вторая команда изменяет именованное значение с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="da58d-110">The second command modifies the named value that has the ID Property11.</span></span>
<span data-ttu-id="da58d-111">Команда назначает строки в $Tags как теги для именованного значения.</span><span class="sxs-lookup"><span data-stu-id="da58d-111">The command assigns the strings in $Tags as tags on the named value.</span></span>

### <span data-ttu-id="da58d-112">Пример 2: изменение именованного значения таким образом, чтобы оно имело секретное значение</span><span class="sxs-lookup"><span data-stu-id="da58d-112">Example 2: Modify the named value to have a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="da58d-113">Эта команда изменяет именованное значение на Encrypt.</span><span class="sxs-lookup"><span data-stu-id="da58d-113">This command changes the named value to be Encrypted.</span></span>

### <span data-ttu-id="da58d-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="da58d-114">Example 3</span></span>

<span data-ttu-id="da58d-115">Изменяет именованное значение для управления API.</span><span class="sxs-lookup"><span data-stu-id="da58d-115">Modifies an API Management Named Value.</span></span> <span data-ttu-id="da58d-116">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="da58d-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementNamedValue -Context <PsApiManagementContext> -Name 'ContosoApi' -NamedValueId 'Property11' -Secret $true -Tag <String[]> -Value 'Property Value'
```

## <span data-ttu-id="da58d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da58d-117">PARAMETERS</span></span>

### <span data-ttu-id="da58d-118">-Context</span><span class="sxs-lookup"><span data-stu-id="da58d-118">-Context</span></span>
<span data-ttu-id="da58d-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="da58d-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="da58d-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="da58d-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da58d-121">-DefaultProfile</span></span>
<span data-ttu-id="da58d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da58d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da58d-123">-Name</span></span>
<span data-ttu-id="da58d-124">Имя именованного значения.</span><span class="sxs-lookup"><span data-stu-id="da58d-124">Name of the named value.</span></span>
<span data-ttu-id="da58d-125">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="da58d-125">Maximum length is 100 characters.</span></span>
<span data-ttu-id="da58d-126">Оно может содержать только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="da58d-126">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="da58d-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="da58d-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-128">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="da58d-128">-NamedValueId</span></span>
<span data-ttu-id="da58d-129">Идентификатор именованного значения для обновления.</span><span class="sxs-lookup"><span data-stu-id="da58d-129">Identifier of named value to update.</span></span>
<span data-ttu-id="da58d-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="da58d-130">This parameter is mandatory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da58d-131">-PassThru</span></span>
<span data-ttu-id="da58d-132">Если указан, то экземпляр Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty, который представляет модифицированное свойство, будет записываться в Output.</span><span class="sxs-lookup"><span data-stu-id="da58d-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty type representing the modified property will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-133">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="da58d-133">-Secret</span></span>
<span data-ttu-id="da58d-134">Является ли именованное значение секретным, и его значение должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="da58d-134">Whether the named value is a secret and its value should be encrypted.</span></span>
<span data-ttu-id="da58d-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="da58d-135">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="da58d-136">-Tag</span></span>
<span data-ttu-id="da58d-137">Теги, связанные с именованным значением.</span><span class="sxs-lookup"><span data-stu-id="da58d-137">Tags associated with the named value.</span></span>
<span data-ttu-id="da58d-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="da58d-138">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-139">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="da58d-139">-Value</span></span>
<span data-ttu-id="da58d-140">Значение именованного значения.</span><span class="sxs-lookup"><span data-stu-id="da58d-140">Value of the named value.</span></span>
<span data-ttu-id="da58d-141">Может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="da58d-141">Can contain policy expressions.</span></span>
<span data-ttu-id="da58d-142">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="da58d-142">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="da58d-143">Оно не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="da58d-143">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="da58d-144">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="da58d-144">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da58d-145">-Confirm</span></span>
<span data-ttu-id="da58d-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da58d-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da58d-147">-WhatIf</span></span>
<span data-ttu-id="da58d-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da58d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da58d-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da58d-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da58d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da58d-150">CommonParameters</span></span>
<span data-ttu-id="da58d-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da58d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da58d-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da58d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da58d-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da58d-153">INPUTS</span></span>

### <span data-ttu-id="da58d-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da58d-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da58d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="da58d-155">System.String</span></span>

### <span data-ttu-id="da58d-156">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="da58d-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="da58d-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="da58d-157">System.String[]</span></span>

### <span data-ttu-id="da58d-158">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="da58d-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="da58d-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da58d-159">OUTPUTS</span></span>

### <span data-ttu-id="da58d-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="da58d-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="da58d-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="da58d-161">NOTES</span></span>

## <span data-ttu-id="da58d-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da58d-162">RELATED LINKS</span></span>