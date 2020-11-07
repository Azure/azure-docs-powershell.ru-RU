---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 49b86055c185dd474499cf8674a34668f69ee060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727923"
---
# <span data-ttu-id="01283-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="01283-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="01283-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01283-102">SYNOPSIS</span></span>
<span data-ttu-id="01283-103">Изменяет свойство управления API.</span><span class="sxs-lookup"><span data-stu-id="01283-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="01283-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01283-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01283-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01283-105">DESCRIPTION</span></span>
<span data-ttu-id="01283-106">Командлет **Set-AzApiManagementProperty** изменяет свойство управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="01283-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="01283-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01283-107">EXAMPLES</span></span>

### <span data-ttu-id="01283-108">Пример 1: изменение тегов в свойстве</span><span class="sxs-lookup"><span data-stu-id="01283-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="01283-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="01283-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="01283-110">Вторая команда изменяет свойство с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="01283-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="01283-111">Команда назначает строки в $Tags в качестве тегов в свойстве.</span><span class="sxs-lookup"><span data-stu-id="01283-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="01283-112">Пример 2: изменение свойства для его секретного значения</span><span class="sxs-lookup"><span data-stu-id="01283-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="01283-113">Эта команда изменяет свойство на зашифрование.</span><span class="sxs-lookup"><span data-stu-id="01283-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="01283-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01283-114">PARAMETERS</span></span>

### <span data-ttu-id="01283-115">-Context</span><span class="sxs-lookup"><span data-stu-id="01283-115">-Context</span></span>
<span data-ttu-id="01283-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="01283-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="01283-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01283-117">-DefaultProfile</span></span>
<span data-ttu-id="01283-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01283-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01283-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01283-119">-Name</span></span>
<span data-ttu-id="01283-120">Указывает имя свойства.</span><span class="sxs-lookup"><span data-stu-id="01283-120">Specifies the name of the property.</span></span>
<span data-ttu-id="01283-121">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="01283-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="01283-122">Имена содержат только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="01283-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="01283-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01283-123">-PassThru</span></span>
<span data-ttu-id="01283-124">Указывает на то, что этот командлет возвращает **PsApiManagementProperty** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="01283-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="01283-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="01283-125">-PropertyId</span></span>
<span data-ttu-id="01283-126">Указывает идентификатор свойства, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="01283-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="01283-127">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="01283-127">-Secret</span></span>
<span data-ttu-id="01283-128">Указывает на то, что значение свойства является секретным и должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="01283-128">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="01283-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="01283-129">-Tag</span></span>
<span data-ttu-id="01283-130">Теги, связанные с свойством.</span><span class="sxs-lookup"><span data-stu-id="01283-130">Tags associated with a property.</span></span> <span data-ttu-id="01283-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="01283-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="01283-132">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="01283-132">-Value</span></span>
<span data-ttu-id="01283-133">Задает значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="01283-133">Specifies a value for the property.</span></span>
<span data-ttu-id="01283-134">Это значение может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="01283-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="01283-135">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="01283-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="01283-136">Значение не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="01283-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="01283-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01283-137">-Confirm</span></span>
<span data-ttu-id="01283-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01283-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01283-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01283-139">-WhatIf</span></span>
<span data-ttu-id="01283-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01283-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01283-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01283-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01283-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01283-142">CommonParameters</span></span>
<span data-ttu-id="01283-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01283-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01283-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01283-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01283-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01283-145">INPUTS</span></span>

### <span data-ttu-id="01283-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01283-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01283-147">System. String</span><span class="sxs-lookup"><span data-stu-id="01283-147">System.String</span></span>

### <span data-ttu-id="01283-148">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="01283-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="01283-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="01283-149">System.String[]</span></span>

### <span data-ttu-id="01283-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="01283-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="01283-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01283-151">OUTPUTS</span></span>

### <span data-ttu-id="01283-152">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="01283-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="01283-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="01283-153">NOTES</span></span>

## <span data-ttu-id="01283-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01283-154">RELATED LINKS</span></span>

[<span data-ttu-id="01283-155">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="01283-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="01283-156">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="01283-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="01283-157">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="01283-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


