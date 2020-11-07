---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 89612136023173d2f725c8c4b286a270400f8c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734193"
---
# <span data-ttu-id="31e5e-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31e5e-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="31e5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="31e5e-103">Изменяет свойство управления API.</span><span class="sxs-lookup"><span data-stu-id="31e5e-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31e5e-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31e5e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="31e5e-106">Командлет **Set-AzureRmApiManagementProperty** изменяет свойство управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="31e5e-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="31e5e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="31e5e-108">Пример 1: изменение тегов в свойстве</span><span class="sxs-lookup"><span data-stu-id="31e5e-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="31e5e-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="31e5e-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="31e5e-110">Вторая команда изменяет свойство с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="31e5e-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="31e5e-111">Команда назначает строки в $Tags в качестве тегов в свойстве.</span><span class="sxs-lookup"><span data-stu-id="31e5e-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="31e5e-112">Пример 2: изменение свойства для его секретного значения</span><span class="sxs-lookup"><span data-stu-id="31e5e-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="31e5e-113">Эта команда изменяет свойство на зашифрование.</span><span class="sxs-lookup"><span data-stu-id="31e5e-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="31e5e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31e5e-114">PARAMETERS</span></span>

### <span data-ttu-id="31e5e-115">-Context</span><span class="sxs-lookup"><span data-stu-id="31e5e-115">-Context</span></span>
<span data-ttu-id="31e5e-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="31e5e-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e5e-117">-DefaultProfile</span></span>
<span data-ttu-id="31e5e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31e5e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e5e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31e5e-119">-Name</span></span>
<span data-ttu-id="31e5e-120">Указывает имя свойства.</span><span class="sxs-lookup"><span data-stu-id="31e5e-120">Specifies the name of the property.</span></span>
<span data-ttu-id="31e5e-121">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="31e5e-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="31e5e-122">Имена содержат только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="31e5e-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e5e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31e5e-123">-PassThru</span></span>
<span data-ttu-id="31e5e-124">Указывает на то, что этот командлет возвращает **PsApiManagementProperty** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="31e5e-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e5e-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="31e5e-125">-PropertyId</span></span>
<span data-ttu-id="31e5e-126">Указывает идентификатор свойства, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="31e5e-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31e5e-127">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="31e5e-127">-Secret</span></span>
<span data-ttu-id="31e5e-128">Указывает на то, что значение свойства является секретным и должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="31e5e-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e5e-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="31e5e-129">-Tag</span></span>
<span data-ttu-id="31e5e-130">Теги, связанные с свойством.</span><span class="sxs-lookup"><span data-stu-id="31e5e-130">Tags associated with a property.</span></span> <span data-ttu-id="31e5e-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="31e5e-131">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e5e-132">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="31e5e-132">-Value</span></span>
<span data-ttu-id="31e5e-133">Задает значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="31e5e-133">Specifies a value for the property.</span></span>
<span data-ttu-id="31e5e-134">Это значение может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="31e5e-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="31e5e-135">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="31e5e-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="31e5e-136">Значение не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="31e5e-136">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e5e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e5e-137">CommonParameters</span></span>
<span data-ttu-id="31e5e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31e5e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e5e-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e5e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e5e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31e5e-140">INPUTS</span></span>

### <span data-ttu-id="31e5e-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="31e5e-141">None</span></span>
<span data-ttu-id="31e5e-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="31e5e-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31e5e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31e5e-143">OUTPUTS</span></span>

### <span data-ttu-id="31e5e-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31e5e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="31e5e-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="31e5e-145">NOTES</span></span>

## <span data-ttu-id="31e5e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31e5e-146">RELATED LINKS</span></span>

[<span data-ttu-id="31e5e-147">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31e5e-147">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="31e5e-148">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31e5e-148">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="31e5e-149">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31e5e-149">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


