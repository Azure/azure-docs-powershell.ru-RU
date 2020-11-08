---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079280"
---
# <span data-ttu-id="77fc5-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="77fc5-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="77fc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="77fc5-103">Возвращает сведения о смарт-группах</span><span class="sxs-lookup"><span data-stu-id="77fc5-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="77fc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77fc5-104">SYNTAX</span></span>

### <span data-ttu-id="77fc5-105">SmartGroupsListByFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77fc5-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77fc5-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="77fc5-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77fc5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77fc5-107">DESCRIPTION</span></span>
<span data-ttu-id="77fc5-108">Командлет **Get-AzSmartGroup** получает сведения о интеллектуальных группах.</span><span class="sxs-lookup"><span data-stu-id="77fc5-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="77fc5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77fc5-109">EXAMPLES</span></span>

### <span data-ttu-id="77fc5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77fc5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="77fc5-111">Список всех интеллектуальных групп, сформированных за последние 1 час.</span><span class="sxs-lookup"><span data-stu-id="77fc5-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="77fc5-112">Используйте Format-List для получения подробных сведений о каждой смарт-группе в списке.</span><span class="sxs-lookup"><span data-stu-id="77fc5-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="77fc5-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="77fc5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="77fc5-114">Получение сведений о Smart Group по идентификатору (GUID) или идентификатору ресурса (полный идентификатор ARM)</span><span class="sxs-lookup"><span data-stu-id="77fc5-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="77fc5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77fc5-115">PARAMETERS</span></span>

### <span data-ttu-id="77fc5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fc5-116">-DefaultProfile</span></span>
<span data-ttu-id="77fc5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77fc5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77fc5-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="77fc5-118">-SmartGroupId</span></span>
<span data-ttu-id="77fc5-119">Уникальный идентификатор SmartGroupа/ResourceId of SmartGroup.</span><span class="sxs-lookup"><span data-stu-id="77fc5-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="77fc5-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="77fc5-120">-SortBy</span></span>
<span data-ttu-id="77fc5-121">Свойство Alert для использования во время сортировки</span><span class="sxs-lookup"><span data-stu-id="77fc5-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="77fc5-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="77fc5-122">-SortOrder</span></span>
<span data-ttu-id="77fc5-123">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="77fc5-123">Sort Order</span></span>

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

### <span data-ttu-id="77fc5-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="77fc5-124">-TimeRange</span></span>
<span data-ttu-id="77fc5-125">Поддерживаемые значения временных диапазонов: 1ч, 1Д, 7D, 30d (значение по умолчанию — 1д)</span><span class="sxs-lookup"><span data-stu-id="77fc5-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="77fc5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fc5-126">CommonParameters</span></span>
<span data-ttu-id="77fc5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77fc5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fc5-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77fc5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fc5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77fc5-129">INPUTS</span></span>

### <span data-ttu-id="77fc5-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="77fc5-130">None</span></span>

## <span data-ttu-id="77fc5-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77fc5-131">OUTPUTS</span></span>

### <span data-ttu-id="77fc5-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="77fc5-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="77fc5-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="77fc5-133">NOTES</span></span>

## <span data-ttu-id="77fc5-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77fc5-134">RELATED LINKS</span></span>
