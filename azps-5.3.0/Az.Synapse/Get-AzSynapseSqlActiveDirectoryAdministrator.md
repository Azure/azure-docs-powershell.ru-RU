---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424468"
---
# <span data-ttu-id="57e45-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="57e45-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="57e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e45-102">SYNOPSIS</span></span>
<span data-ttu-id="57e45-103">Сведения о администраторе Azure AD в рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="57e45-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="57e45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57e45-104">SYNTAX</span></span>

### <span data-ttu-id="57e45-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57e45-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57e45-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57e45-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57e45-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57e45-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57e45-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57e45-108">DESCRIPTION</span></span>
<span data-ttu-id="57e45-109">Чтобы получить сведения о администраторе Azure Active Directory (Azure AD) для рабочей области Azure Synapse Analytics в текущей подписке, можно получить сведения о том, как получить сведения о администраторе **Get-AzSynapseSqlActiveDirectoryAdministrator.**</span><span class="sxs-lookup"><span data-stu-id="57e45-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="57e45-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57e45-110">EXAMPLES</span></span>

### <span data-ttu-id="57e45-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57e45-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="57e45-112">Эта команда получает сведения о администраторе Azure AD для рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="57e45-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="57e45-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57e45-113">PARAMETERS</span></span>

### <span data-ttu-id="57e45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e45-114">-DefaultProfile</span></span>
<span data-ttu-id="57e45-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57e45-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57e45-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57e45-116">-InputObject</span></span>
<span data-ttu-id="57e45-117">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="57e45-117">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57e45-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e45-118">-ResourceGroupName</span></span>
<span data-ttu-id="57e45-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57e45-119">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e45-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57e45-120">-ResourceId</span></span>
<span data-ttu-id="57e45-121">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="57e45-121">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e45-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="57e45-122">-WorkspaceName</span></span>
<span data-ttu-id="57e45-123">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="57e45-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e45-124">CommonParameters</span></span>
<span data-ttu-id="57e45-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e45-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57e45-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e45-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57e45-127">INPUTS</span></span>

### <span data-ttu-id="57e45-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="57e45-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="57e45-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57e45-129">OUTPUTS</span></span>

### <span data-ttu-id="57e45-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="57e45-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="57e45-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57e45-131">NOTES</span></span>

## <span data-ttu-id="57e45-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57e45-132">RELATED LINKS</span></span>
