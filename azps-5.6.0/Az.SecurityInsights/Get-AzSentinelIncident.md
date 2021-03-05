---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: 669e0961327b6419e86f288ec71bffa6cdc69b4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986443"
---
# <span data-ttu-id="b0c2c-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="b0c2c-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="b0c2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c2c-103">Получить инцидент.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-103">Get an Incident.</span></span>

## <span data-ttu-id="b0c2c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0c2c-104">SYNTAX</span></span>

### <span data-ttu-id="b0c2c-105">WorkspaceScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0c2c-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0c2c-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="b0c2c-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0c2c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0c2c-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0c2c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0c2c-108">DESCRIPTION</span></span>
<span data-ttu-id="b0c2c-109">**Cmdlet Get-AzSentinelIncident** получает инцидент из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="b0c2c-110">Если указать параметр *IncidentId,* возвращается один объект **IncidentId.**</span><span class="sxs-lookup"><span data-stu-id="b0c2c-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="b0c2c-111">Если не указать параметр *IncidentId,* возвращается массив, содержащий все инциденты в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="b0c2c-112">Вы можете обновить **инцидент** с помощью объекта "Инцидент", например добавить заметки к **инциденту.**</span><span class="sxs-lookup"><span data-stu-id="b0c2c-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="b0c2c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0c2c-113">EXAMPLES</span></span>

### <span data-ttu-id="b0c2c-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0c2c-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="b0c2c-115">В этом примере  все инциденты в указанной рабочей области получаются, а затем в переменной $Incidents сохраняется.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="b0c2c-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b0c2c-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="b0c2c-117">В этом примере **в указанной** рабочей области возвращается инцидент, который затем сохраняется $Incident переменной.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="b0c2c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0c2c-118">PARAMETERS</span></span>

### <span data-ttu-id="b0c2c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c2c-119">-DefaultProfile</span></span>
<span data-ttu-id="b0c2c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0c2c-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="b0c2c-121">-IncidentId</span></span>
<span data-ttu-id="b0c2c-122">ИД инцидента.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0c2c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c2c-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0c2c-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c2c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0c2c-125">-ResourceId</span></span>
<span data-ttu-id="b0c2c-126">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0c2c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0c2c-127">-WorkspaceName</span></span>
<span data-ttu-id="b0c2c-128">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c2c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c2c-129">CommonParameters</span></span>
<span data-ttu-id="b0c2c-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c2c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c2c-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0c2c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c2c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0c2c-132">INPUTS</span></span>

### <span data-ttu-id="b0c2c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b0c2c-133">System.String</span></span>
## <span data-ttu-id="b0c2c-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0c2c-134">OUTPUTS</span></span>

### <span data-ttu-id="b0c2c-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="b0c2c-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="b0c2c-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0c2c-136">NOTES</span></span>

## <span data-ttu-id="b0c2c-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0c2c-137">RELATED LINKS</span></span>
