---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225281"
---
# <span data-ttu-id="8770a-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="8770a-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="8770a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8770a-102">SYNOPSIS</span></span>
<span data-ttu-id="8770a-103">Создайте объект "Владелец инцидента", чтобы обновить владельца инцидента.</span><span class="sxs-lookup"><span data-stu-id="8770a-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="8770a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8770a-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8770a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8770a-105">DESCRIPTION</span></span>
<span data-ttu-id="8770a-106">Для **обновления инцидента новый-AzSentinelIncidentOwner** создает объект "Владелец инцидента" в памяти.</span><span class="sxs-lookup"><span data-stu-id="8770a-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="8770a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8770a-107">EXAMPLES</span></span>

### <span data-ttu-id="8770a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8770a-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="8770a-109">В этом примере создается **владелец инцидентов,** который обновляет инцидент для нового владельца.</span><span class="sxs-lookup"><span data-stu-id="8770a-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="8770a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8770a-110">PARAMETERS</span></span>

### <span data-ttu-id="8770a-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="8770a-111">-AssignedTo</span></span>
<span data-ttu-id="8770a-112">Владелец инцидента — назначено</span><span class="sxs-lookup"><span data-stu-id="8770a-112">Incident Owner - Assigned To</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8770a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8770a-113">-DefaultProfile</span></span>
<span data-ttu-id="8770a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8770a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8770a-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="8770a-115">-Email</span></span>
<span data-ttu-id="8770a-116">Владелец инцидента — электронная почта</span><span class="sxs-lookup"><span data-stu-id="8770a-116">Incident Owner - Email</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8770a-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8770a-117">-ObjectId</span></span>
<span data-ttu-id="8770a-118">Владелец инцидента — ObjectId</span><span class="sxs-lookup"><span data-stu-id="8770a-118">Incident Owner - ObjectId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8770a-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8770a-119">-UserPrincipalName</span></span>
<span data-ttu-id="8770a-120">Владелец инцидента — имя директора-пользователя</span><span class="sxs-lookup"><span data-stu-id="8770a-120">Incident Owner - User Principal Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8770a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8770a-121">CommonParameters</span></span>
<span data-ttu-id="8770a-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8770a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8770a-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8770a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8770a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8770a-124">INPUTS</span></span>

### <span data-ttu-id="8770a-125">Нет</span><span class="sxs-lookup"><span data-stu-id="8770a-125">None</span></span>
## <span data-ttu-id="8770a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8770a-126">OUTPUTS</span></span>

### <span data-ttu-id="8770a-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8770a-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="8770a-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8770a-128">NOTES</span></span>

## <span data-ttu-id="8770a-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8770a-129">RELATED LINKS</span></span>
