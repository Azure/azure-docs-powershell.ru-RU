---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400711"
---
# <span data-ttu-id="36192-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="36192-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="36192-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36192-102">SYNOPSIS</span></span>
<span data-ttu-id="36192-103">Создание именоваемой стоимости.</span><span class="sxs-lookup"><span data-stu-id="36192-103">Creates new Named Value.</span></span>

## <span data-ttu-id="36192-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36192-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36192-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36192-105">DESCRIPTION</span></span>
<span data-ttu-id="36192-106">Для создания именоваемого значения управления API Azure создается новый клиент **AzApiManagementNamedValue.**</span><span class="sxs-lookup"><span data-stu-id="36192-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="36192-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36192-107">EXAMPLES</span></span>

### <span data-ttu-id="36192-108">Пример 1. Создание именоваемой величины с тегами</span><span class="sxs-lookup"><span data-stu-id="36192-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="36192-109">Первая команда назначает два значения переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="36192-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="36192-110">Вторая команда создает именуемом значении и назначает строки в $Tags в качестве тегов свойства.</span><span class="sxs-lookup"><span data-stu-id="36192-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="36192-111">Пример 2. Создание именоваемой величины, которая имеет секретное значение</span><span class="sxs-lookup"><span data-stu-id="36192-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="36192-112">Эта команда создает **именуемую величину** со значением, зашифрованным.</span><span class="sxs-lookup"><span data-stu-id="36192-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="36192-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36192-113">PARAMETERS</span></span>

### <span data-ttu-id="36192-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="36192-114">-Context</span></span>
<span data-ttu-id="36192-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="36192-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="36192-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="36192-116">This parameter is required.</span></span>

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

### <span data-ttu-id="36192-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36192-117">-DefaultProfile</span></span>
<span data-ttu-id="36192-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36192-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36192-119">-Name</span><span class="sxs-lookup"><span data-stu-id="36192-119">-Name</span></span>
<span data-ttu-id="36192-120">Имя именуемого значения.</span><span class="sxs-lookup"><span data-stu-id="36192-120">Name of the named value.</span></span>
<span data-ttu-id="36192-121">Максимальная длина составляет 100 знаков.</span><span class="sxs-lookup"><span data-stu-id="36192-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="36192-122">Оно может содержать только буквы, цифры, тире, тире и символы подчеркиваия.</span><span class="sxs-lookup"><span data-stu-id="36192-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="36192-123">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="36192-123">This parameter is required.</span></span>

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

### <span data-ttu-id="36192-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="36192-124">-NamedValueId</span></span>
<span data-ttu-id="36192-125">Идентификатор нового именоваемого значения.</span><span class="sxs-lookup"><span data-stu-id="36192-125">Identifier of new named value.</span></span>
<span data-ttu-id="36192-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="36192-126">This parameter is optional.</span></span>
<span data-ttu-id="36192-127">Если он не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="36192-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="36192-128">-Секретная</span><span class="sxs-lookup"><span data-stu-id="36192-128">-Secret</span></span>
<span data-ttu-id="36192-129">Определяет, является ли значение секретным и должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="36192-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="36192-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="36192-130">This parameter is optional.</span></span>
<span data-ttu-id="36192-131">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="36192-131">Default Value is false.</span></span>

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

### <span data-ttu-id="36192-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="36192-132">-Tag</span></span>
<span data-ttu-id="36192-133">Теги, связанные с именованым значением.</span><span class="sxs-lookup"><span data-stu-id="36192-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="36192-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="36192-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="36192-135">-Value</span><span class="sxs-lookup"><span data-stu-id="36192-135">-Value</span></span>
<span data-ttu-id="36192-136">Значение именуемого значения.</span><span class="sxs-lookup"><span data-stu-id="36192-136">Value of the named value.</span></span>
<span data-ttu-id="36192-137">Может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="36192-137">Can contain policy expressions.</span></span>
<span data-ttu-id="36192-138">Максимальная длина — 1000 знаков.</span><span class="sxs-lookup"><span data-stu-id="36192-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="36192-139">Оно не может быть пустым или включать только пустое пространство.</span><span class="sxs-lookup"><span data-stu-id="36192-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="36192-140">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="36192-140">This parameter is required.</span></span>

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

### <span data-ttu-id="36192-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36192-141">-Confirm</span></span>
<span data-ttu-id="36192-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="36192-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36192-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36192-143">-WhatIf</span></span>
<span data-ttu-id="36192-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36192-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36192-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36192-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36192-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36192-146">CommonParameters</span></span>
<span data-ttu-id="36192-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36192-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36192-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36192-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36192-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36192-149">INPUTS</span></span>

### <span data-ttu-id="36192-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36192-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36192-151">System.String</span><span class="sxs-lookup"><span data-stu-id="36192-151">System.String</span></span>

### <span data-ttu-id="36192-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36192-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="36192-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="36192-153">System.String[]</span></span>

## <span data-ttu-id="36192-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36192-154">OUTPUTS</span></span>

### <span data-ttu-id="36192-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="36192-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="36192-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36192-156">NOTES</span></span>

## <span data-ttu-id="36192-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36192-157">RELATED LINKS</span></span>
