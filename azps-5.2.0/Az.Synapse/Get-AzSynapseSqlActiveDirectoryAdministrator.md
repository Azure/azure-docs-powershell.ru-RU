---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393836"
---
# <span data-ttu-id="16235-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="16235-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="16235-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16235-102">SYNOPSIS</span></span>
<span data-ttu-id="16235-103">Сведения о администраторе Azure AD в рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="16235-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="16235-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16235-104">SYNTAX</span></span>

### <span data-ttu-id="16235-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16235-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16235-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16235-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16235-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16235-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16235-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16235-108">DESCRIPTION</span></span>
<span data-ttu-id="16235-109">Чтобы получить сведения о администраторе Azure Active Directory (Azure AD) для рабочей области Azure Synapse Analytics в текущей подписке, можно получить сведения о **get-AzSynapseSqlActiveDirectoryAdministrator.**</span><span class="sxs-lookup"><span data-stu-id="16235-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="16235-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16235-110">EXAMPLES</span></span>

### <span data-ttu-id="16235-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16235-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="16235-112">Эта команда получает сведения о администраторе Azure AD для рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="16235-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="16235-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16235-113">PARAMETERS</span></span>

### <span data-ttu-id="16235-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16235-114">-DefaultProfile</span></span>
<span data-ttu-id="16235-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16235-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16235-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16235-116">-InputObject</span></span>
<span data-ttu-id="16235-117">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="16235-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="16235-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16235-118">-ResourceGroupName</span></span>
<span data-ttu-id="16235-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16235-119">Resource group name.</span></span>

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

### <span data-ttu-id="16235-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16235-120">-ResourceId</span></span>
<span data-ttu-id="16235-121">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="16235-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="16235-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="16235-122">-WorkspaceName</span></span>
<span data-ttu-id="16235-123">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="16235-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="16235-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16235-124">CommonParameters</span></span>
<span data-ttu-id="16235-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16235-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16235-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16235-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16235-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16235-127">INPUTS</span></span>

### <span data-ttu-id="16235-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="16235-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="16235-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16235-129">OUTPUTS</span></span>

### <span data-ttu-id="16235-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="16235-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="16235-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16235-131">NOTES</span></span>

## <span data-ttu-id="16235-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16235-132">RELATED LINKS</span></span>