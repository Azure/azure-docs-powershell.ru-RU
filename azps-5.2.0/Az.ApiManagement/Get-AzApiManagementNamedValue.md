---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403932"
---
# <span data-ttu-id="5e654-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="5e654-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="5e654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e654-102">SYNOPSIS</span></span>
<span data-ttu-id="5e654-103">Возвращает список или определенное именуемом значении.</span><span class="sxs-lookup"><span data-stu-id="5e654-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="5e654-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5e654-104">SYNTAX</span></span>

### <span data-ttu-id="5e654-105">GetAllNamedValues (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e654-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e654-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="5e654-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e654-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="5e654-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e654-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="5e654-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e654-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e654-109">DESCRIPTION</span></span>
<span data-ttu-id="5e654-110">Для получения списка или определенного именового значения с его названием возвращается **cmdlet Get-AzApiManagementNamedValue.**</span><span class="sxs-lookup"><span data-stu-id="5e654-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="5e654-111">Значение не включается в сведения о результатах, если именованое значение помечено как секрет.</span><span class="sxs-lookup"><span data-stu-id="5e654-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="5e654-112">Чтобы получить секретное значение, используйте **Get-AzApiManagementNamedValueSecretValue.**</span><span class="sxs-lookup"><span data-stu-id="5e654-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="5e654-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5e654-113">EXAMPLES</span></span>

### <span data-ttu-id="5e654-114">Пример 1. Получить именуемую величину по имени</span><span class="sxs-lookup"><span data-stu-id="5e654-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="5e654-115">Эта команда получает сведения об именоваемом значении с именем.</span><span class="sxs-lookup"><span data-stu-id="5e654-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="5e654-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e654-116">PARAMETERS</span></span>

### <span data-ttu-id="5e654-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="5e654-117">-Context</span></span>
<span data-ttu-id="5e654-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5e654-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5e654-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="5e654-119">This parameter is required.</span></span>

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

### <span data-ttu-id="5e654-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e654-120">-DefaultProfile</span></span>
<span data-ttu-id="5e654-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e654-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e654-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5e654-122">-Name</span></span>
<span data-ttu-id="5e654-123">Находит именные значения с именами, содержащими строку "Имя".</span><span class="sxs-lookup"><span data-stu-id="5e654-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="5e654-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5e654-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e654-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="5e654-125">-NamedValueId</span></span>
<span data-ttu-id="5e654-126">Идентификатор именуемого значения.</span><span class="sxs-lookup"><span data-stu-id="5e654-126">Identifier of the named value.</span></span>
<span data-ttu-id="5e654-127">Если он указан, будет пытаться найти указанное значение по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="5e654-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="5e654-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5e654-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e654-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e654-129">-Tag</span></span>
<span data-ttu-id="5e654-130">Находит именуемые значения, связанные с тегом.</span><span class="sxs-lookup"><span data-stu-id="5e654-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="5e654-131">Если указано, будут возвращены все свойства, связанные с тегом.</span><span class="sxs-lookup"><span data-stu-id="5e654-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="5e654-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5e654-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e654-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e654-133">CommonParameters</span></span>
<span data-ttu-id="5e654-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e654-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e654-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e654-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e654-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e654-136">INPUTS</span></span>

### <span data-ttu-id="5e654-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5e654-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5e654-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5e654-138">System.String</span></span>

## <span data-ttu-id="5e654-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e654-139">OUTPUTS</span></span>

### <span data-ttu-id="5e654-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="5e654-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="5e654-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5e654-141">NOTES</span></span>

## <span data-ttu-id="5e654-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e654-142">RELATED LINKS</span></span>
