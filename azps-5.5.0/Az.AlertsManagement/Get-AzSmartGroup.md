---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233865"
---
# <span data-ttu-id="00f3a-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="00f3a-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="00f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="00f3a-103">Получает сведения о интеллектуальных группах</span><span class="sxs-lookup"><span data-stu-id="00f3a-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="00f3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="00f3a-104">SYNTAX</span></span>

### <span data-ttu-id="00f3a-105">SmartGroupsListByFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00f3a-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00f3a-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="00f3a-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00f3a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00f3a-107">DESCRIPTION</span></span>
<span data-ttu-id="00f3a-108">**Для получения сведений из смарт-групп в Get-AzSmartGroup** требуется информация из интеллектуальных групп.</span><span class="sxs-lookup"><span data-stu-id="00f3a-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="00f3a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="00f3a-109">EXAMPLES</span></span>

### <span data-ttu-id="00f3a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00f3a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="00f3a-111">Список всех интеллектуальных групп, сформированных за последние 1 час.</span><span class="sxs-lookup"><span data-stu-id="00f3a-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="00f3a-112">Используйте Format-List, чтобы получить полные сведения о каждой интеллектуальной группе в списке.</span><span class="sxs-lookup"><span data-stu-id="00f3a-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="00f3a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="00f3a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="00f3a-114">Получите сведения о смарт-группе по ИД (GUID) или ид ресурса (ARM завершения)</span><span class="sxs-lookup"><span data-stu-id="00f3a-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="00f3a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00f3a-115">PARAMETERS</span></span>

### <span data-ttu-id="00f3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f3a-116">-DefaultProfile</span></span>
<span data-ttu-id="00f3a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00f3a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f3a-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="00f3a-118">-SmartGroupId</span></span>
<span data-ttu-id="00f3a-119">Уникальный идентификатор SmartGroup и ResourceId этой группы.</span><span class="sxs-lookup"><span data-stu-id="00f3a-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f3a-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="00f3a-120">-SortBy</span></span>
<span data-ttu-id="00f3a-121">Свойство оповещения, используемее при сортировке</span><span class="sxs-lookup"><span data-stu-id="00f3a-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f3a-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="00f3a-122">-SortOrder</span></span>
<span data-ttu-id="00f3a-123">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="00f3a-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f3a-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="00f3a-124">-TimeRange</span></span>
<span data-ttu-id="00f3a-125">Поддерживаемые значения диапазонов времени: 1h, 1d, 7d, 30d (значение по умолчанию — 1d)</span><span class="sxs-lookup"><span data-stu-id="00f3a-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f3a-126">CommonParameters</span></span>
<span data-ttu-id="00f3a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f3a-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00f3a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f3a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00f3a-129">INPUTS</span></span>

### <span data-ttu-id="00f3a-130">Нет</span><span class="sxs-lookup"><span data-stu-id="00f3a-130">None</span></span>

## <span data-ttu-id="00f3a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="00f3a-131">OUTPUTS</span></span>

### <span data-ttu-id="00f3a-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="00f3a-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="00f3a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="00f3a-133">NOTES</span></span>

## <span data-ttu-id="00f3a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00f3a-134">RELATED LINKS</span></span>
