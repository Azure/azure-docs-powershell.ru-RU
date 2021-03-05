---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: 61ddc7c6a71dcc5545b8bdc2751e619d7da8e3bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967219"
---
# <span data-ttu-id="1e61b-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="1e61b-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="1e61b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e61b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e61b-103">Получает сведения о связанных службах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1e61b-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="1e61b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e61b-104">SYNTAX</span></span>

### <span data-ttu-id="1e61b-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e61b-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e61b-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="1e61b-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e61b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e61b-107">DESCRIPTION</span></span>
<span data-ttu-id="1e61b-108">Чтобы получить сведения о связанных службах в рабочей области, можно получить сведения о **get-AzSynapseLinkedService.**</span><span class="sxs-lookup"><span data-stu-id="1e61b-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="1e61b-109">Если указать имя связанной службы, этот cmdlet получит сведения о связанной службе.</span><span class="sxs-lookup"><span data-stu-id="1e61b-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="1e61b-110">Если имя не указано, этот cmdlet получает сведения обо всех связанных службах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1e61b-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="1e61b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e61b-111">EXAMPLES</span></span>

### <span data-ttu-id="1e61b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e61b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1e61b-113">Эта команда получает сведения обо всех связанных службах в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1e61b-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1e61b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1e61b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="1e61b-115">Эта команда получает сведения о связанной службе ContosoLinkedService в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1e61b-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1e61b-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1e61b-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="1e61b-117">Эта команда получает сведения о связанной службе с именем ContosoLinkedService в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="1e61b-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1e61b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e61b-118">PARAMETERS</span></span>

### <span data-ttu-id="1e61b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e61b-119">-DefaultProfile</span></span>
<span data-ttu-id="1e61b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e61b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e61b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1e61b-121">-Name</span></span>
<span data-ttu-id="1e61b-122">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="1e61b-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e61b-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1e61b-123">-WorkspaceName</span></span>
<span data-ttu-id="1e61b-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="1e61b-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e61b-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1e61b-125">-WorkspaceObject</span></span>
<span data-ttu-id="1e61b-126">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="1e61b-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e61b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e61b-127">CommonParameters</span></span>
<span data-ttu-id="1e61b-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e61b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e61b-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e61b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e61b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e61b-130">INPUTS</span></span>

### <span data-ttu-id="1e61b-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e61b-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1e61b-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e61b-132">OUTPUTS</span></span>

### <span data-ttu-id="1e61b-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="1e61b-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="1e61b-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e61b-134">NOTES</span></span>

## <span data-ttu-id="1e61b-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e61b-135">RELATED LINKS</span></span>
