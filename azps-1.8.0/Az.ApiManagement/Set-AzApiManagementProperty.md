---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: b12a904be944b4a6338ad0bf34a4c906382cb910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901554"
---
# <span data-ttu-id="53006-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="53006-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="53006-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53006-102">SYNOPSIS</span></span>
<span data-ttu-id="53006-103">Изменяет свойство управления API.</span><span class="sxs-lookup"><span data-stu-id="53006-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="53006-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53006-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53006-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53006-105">DESCRIPTION</span></span>
<span data-ttu-id="53006-106">Командлет **Set-AzApiManagementProperty** изменяет свойство управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="53006-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="53006-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53006-107">EXAMPLES</span></span>

### <span data-ttu-id="53006-108">Пример 1: изменение тегов в свойстве</span><span class="sxs-lookup"><span data-stu-id="53006-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="53006-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="53006-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="53006-110">Вторая команда изменяет свойство с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="53006-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="53006-111">Команда назначает строки в $Tags в качестве тегов в свойстве.</span><span class="sxs-lookup"><span data-stu-id="53006-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="53006-112">Пример 2: изменение свойства для его секретного значения</span><span class="sxs-lookup"><span data-stu-id="53006-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="53006-113">Эта команда изменяет свойство на зашифрование.</span><span class="sxs-lookup"><span data-stu-id="53006-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="53006-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53006-114">PARAMETERS</span></span>

### <span data-ttu-id="53006-115">-Context</span><span class="sxs-lookup"><span data-stu-id="53006-115">-Context</span></span>
<span data-ttu-id="53006-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="53006-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53006-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53006-117">-DefaultProfile</span></span>
<span data-ttu-id="53006-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53006-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53006-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53006-119">-Name</span></span>
<span data-ttu-id="53006-120">Указывает имя свойства.</span><span class="sxs-lookup"><span data-stu-id="53006-120">Specifies the name of the property.</span></span>
<span data-ttu-id="53006-121">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="53006-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="53006-122">Имена содержат только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="53006-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="53006-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53006-123">-PassThru</span></span>
<span data-ttu-id="53006-124">Указывает на то, что этот командлет возвращает **PsApiManagementProperty** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="53006-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="53006-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="53006-125">-PropertyId</span></span>
<span data-ttu-id="53006-126">Указывает идентификатор свойства, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="53006-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="53006-127">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="53006-127">-Secret</span></span>
<span data-ttu-id="53006-128">Указывает на то, что значение свойства является секретным и должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="53006-128">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="53006-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="53006-129">-Tag</span></span>
<span data-ttu-id="53006-130">Теги, связанные с свойством.</span><span class="sxs-lookup"><span data-stu-id="53006-130">Tags associated with a property.</span></span> <span data-ttu-id="53006-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="53006-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="53006-132">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="53006-132">-Value</span></span>
<span data-ttu-id="53006-133">Задает значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="53006-133">Specifies a value for the property.</span></span>
<span data-ttu-id="53006-134">Это значение может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="53006-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="53006-135">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="53006-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="53006-136">Значение не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="53006-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="53006-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53006-137">CommonParameters</span></span>
<span data-ttu-id="53006-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53006-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53006-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53006-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53006-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53006-140">INPUTS</span></span>

### <span data-ttu-id="53006-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="53006-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="53006-142">System. String</span><span class="sxs-lookup"><span data-stu-id="53006-142">System.String</span></span>

### <span data-ttu-id="53006-143">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="53006-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="53006-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="53006-144">System.String[]</span></span>

### <span data-ttu-id="53006-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="53006-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="53006-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53006-146">OUTPUTS</span></span>

### <span data-ttu-id="53006-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="53006-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="53006-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="53006-148">NOTES</span></span>

## <span data-ttu-id="53006-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53006-149">RELATED LINKS</span></span>

[<span data-ttu-id="53006-150">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="53006-150">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="53006-151">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="53006-151">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="53006-152">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="53006-152">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


