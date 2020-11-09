---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementNamedValue.md
ms.openlocfilehash: d3902a085ae870034bbb0fbc668d55166b7fe61c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249128"
---
# <span data-ttu-id="78c68-101">Set-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="78c68-101">Set-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="78c68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78c68-102">SYNOPSIS</span></span>
<span data-ttu-id="78c68-103">Изменяет именованное значение для управления API.</span><span class="sxs-lookup"><span data-stu-id="78c68-103">Modifies an API Management Named Value.</span></span>

## <span data-ttu-id="78c68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78c68-104">SYNTAX</span></span>

```
Set-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78c68-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78c68-105">DESCRIPTION</span></span>
<span data-ttu-id="78c68-106">Командлет **Set-AzApiManagementNamedValue** изменяет именованное значение управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="78c68-106">The **Set-AzApiManagementNamedValue** cmdlet modifies an Azure API Management Named Value.</span></span>

## <span data-ttu-id="78c68-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78c68-107">EXAMPLES</span></span>

### <span data-ttu-id="78c68-108">Пример 1: изменение тегов для именованного значения</span><span class="sxs-lookup"><span data-stu-id="78c68-108">Example 1: Change the tags on the named value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="78c68-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="78c68-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="78c68-110">Вторая команда изменяет именованное значение с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="78c68-110">The second command modifies the named value that has the ID Property11.</span></span>
<span data-ttu-id="78c68-111">Команда назначает строки в $Tags как теги для именованного значения.</span><span class="sxs-lookup"><span data-stu-id="78c68-111">The command assigns the strings in $Tags as tags on the named value.</span></span>

### <span data-ttu-id="78c68-112">Пример 2: изменение именованного значения таким образом, чтобы оно имело секретное значение</span><span class="sxs-lookup"><span data-stu-id="78c68-112">Example 2: Modify the named value to have a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="78c68-113">Эта команда изменяет именованное значение на Encrypt.</span><span class="sxs-lookup"><span data-stu-id="78c68-113">This command changes the named value to be Encrypted.</span></span>

### <span data-ttu-id="78c68-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="78c68-114">Example 3</span></span>

<span data-ttu-id="78c68-115">Изменяет именованное значение для управления API.</span><span class="sxs-lookup"><span data-stu-id="78c68-115">Modifies an API Management Named Value.</span></span> <span data-ttu-id="78c68-116">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="78c68-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementNamedValue -Context <PsApiManagementContext> -Name 'ContosoApi' -NamedValueId 'Property11' -Secret $true -Tag <String[]> -Value 'Property Value'
```

## <span data-ttu-id="78c68-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78c68-117">PARAMETERS</span></span>

### <span data-ttu-id="78c68-118">-Context</span><span class="sxs-lookup"><span data-stu-id="78c68-118">-Context</span></span>
<span data-ttu-id="78c68-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="78c68-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="78c68-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="78c68-120">This parameter is required.</span></span>

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

### <span data-ttu-id="78c68-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c68-121">-DefaultProfile</span></span>
<span data-ttu-id="78c68-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78c68-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78c68-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78c68-123">-Name</span></span>
<span data-ttu-id="78c68-124">Имя именованного значения.</span><span class="sxs-lookup"><span data-stu-id="78c68-124">Name of the named value.</span></span>
<span data-ttu-id="78c68-125">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="78c68-125">Maximum length is 100 characters.</span></span>
<span data-ttu-id="78c68-126">Оно может содержать только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="78c68-126">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="78c68-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78c68-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="78c68-128">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="78c68-128">-NamedValueId</span></span>
<span data-ttu-id="78c68-129">Идентификатор именованного значения для обновления.</span><span class="sxs-lookup"><span data-stu-id="78c68-129">Identifier of named value to update.</span></span>
<span data-ttu-id="78c68-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="78c68-130">This parameter is mandatory.</span></span>

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

### <span data-ttu-id="78c68-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78c68-131">-PassThru</span></span>
<span data-ttu-id="78c68-132">Если указан, то экземпляр Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty, который представляет модифицированное свойство, будет записываться в Output.</span><span class="sxs-lookup"><span data-stu-id="78c68-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty type representing the modified property will be written to output.</span></span>

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

### <span data-ttu-id="78c68-133">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="78c68-133">-Secret</span></span>
<span data-ttu-id="78c68-134">Является ли именованное значение секретным, и его значение должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="78c68-134">Whether the named value is a secret and its value should be encrypted.</span></span>
<span data-ttu-id="78c68-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78c68-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="78c68-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="78c68-136">-Tag</span></span>
<span data-ttu-id="78c68-137">Теги, связанные с именованным значением.</span><span class="sxs-lookup"><span data-stu-id="78c68-137">Tags associated with the named value.</span></span>
<span data-ttu-id="78c68-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78c68-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="78c68-139">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="78c68-139">-Value</span></span>
<span data-ttu-id="78c68-140">Значение именованного значения.</span><span class="sxs-lookup"><span data-stu-id="78c68-140">Value of the named value.</span></span>
<span data-ttu-id="78c68-141">Может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="78c68-141">Can contain policy expressions.</span></span>
<span data-ttu-id="78c68-142">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="78c68-142">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="78c68-143">Оно не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="78c68-143">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="78c68-144">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78c68-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="78c68-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78c68-145">-Confirm</span></span>
<span data-ttu-id="78c68-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78c68-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c68-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c68-147">-WhatIf</span></span>
<span data-ttu-id="78c68-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78c68-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78c68-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78c68-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78c68-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c68-150">CommonParameters</span></span>
<span data-ttu-id="78c68-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78c68-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c68-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78c68-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c68-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78c68-153">INPUTS</span></span>

### <span data-ttu-id="78c68-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="78c68-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78c68-155">System. String</span><span class="sxs-lookup"><span data-stu-id="78c68-155">System.String</span></span>

### <span data-ttu-id="78c68-156">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78c68-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="78c68-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="78c68-157">System.String[]</span></span>

### <span data-ttu-id="78c68-158">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78c68-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78c68-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78c68-159">OUTPUTS</span></span>

### <span data-ttu-id="78c68-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="78c68-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="78c68-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="78c68-161">NOTES</span></span>

## <span data-ttu-id="78c68-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78c68-162">RELATED LINKS</span></span>