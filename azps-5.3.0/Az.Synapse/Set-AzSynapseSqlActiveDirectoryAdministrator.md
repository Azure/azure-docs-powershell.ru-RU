---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507946"
---
# <span data-ttu-id="c3928-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c3928-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="c3928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3928-102">SYNOPSIS</span></span>
<span data-ttu-id="c3928-103">Подготовка администратора Azure AD для пула Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="c3928-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c3928-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c3928-104">SYNTAX</span></span>

### <span data-ttu-id="c3928-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3928-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3928-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3928-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3928-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3928-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3928-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3928-108">DESCRIPTION</span></span>
<span data-ttu-id="c3928-109">Для рабочей области Azure Synapse Analytics, которая в текущей подписке является администратором **Set-AzSynapseSqlActiveDirectoryAdministrator,** устанавливается администратор Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c3928-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="c3928-110">Одновременно можно втьть только одного администратора.</span><span class="sxs-lookup"><span data-stu-id="c3928-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="c3928-111">В качестве администратора рабочей области Synapse Analytics можно получить следующих участников Azure AD:</span><span class="sxs-lookup"><span data-stu-id="c3928-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="c3928-112">Участники, которые являются участниками Azure AD</span><span class="sxs-lookup"><span data-stu-id="c3928-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="c3928-113">Федераированные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="c3928-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="c3928-114">Импортированные участники из других служб Azure ADs, которые являются родными или федеративными участниками</span><span class="sxs-lookup"><span data-stu-id="c3928-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="c3928-115">Группы Azure AD, созданные как учетные записи Майкрософт в качестве групп безопасности, например в доменах Outlook.com, Hotmail.com или Live.com, не поддерживаются администраторами.</span><span class="sxs-lookup"><span data-stu-id="c3928-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="c3928-116">Другие гостевых учетные записи, например учетные записи Gmail.com или Yahoo.com, не поддерживаются администраторами.</span><span class="sxs-lookup"><span data-stu-id="c3928-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="c3928-117">Мы рекомендуем на правах администратора использовать специальную группу Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c3928-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="c3928-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c3928-118">EXAMPLES</span></span>

### <span data-ttu-id="c3928-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3928-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="c3928-120">Эта команда предусматривает группу администраторов Azure AD с именем DBAs для рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c3928-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c3928-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c3928-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="c3928-122">Эта команда предусматривает группу администраторов Azure AD с именем DBAs для рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c3928-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="c3928-123">Это позволяет добиться успеха команды, даже если отображаемое имя группы не уникально.</span><span class="sxs-lookup"><span data-stu-id="c3928-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="c3928-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3928-124">PARAMETERS</span></span>

### <span data-ttu-id="c3928-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3928-125">-AsJob</span></span>
<span data-ttu-id="c3928-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c3928-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3928-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3928-127">-DefaultProfile</span></span>
<span data-ttu-id="c3928-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3928-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3928-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c3928-129">-DisplayName</span></span>
<span data-ttu-id="c3928-130">Отображает имя пользователя или группы, для которых нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="c3928-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="c3928-131">Это отображаемая имя должна существовать в активном каталоге, связанном с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="c3928-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="c3928-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3928-132">-InputObject</span></span>
<span data-ttu-id="c3928-133">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="c3928-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3928-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c3928-134">-ObjectId</span></span>
<span data-ttu-id="c3928-135">Определяет ИД объекта пользователя или группы в Azure Active Directory, для которого нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="c3928-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3928-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3928-136">-ResourceGroupName</span></span>
<span data-ttu-id="c3928-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c3928-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3928-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3928-138">-ResourceId</span></span>
<span data-ttu-id="c3928-139">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c3928-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3928-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c3928-140">-WorkspaceName</span></span>
<span data-ttu-id="c3928-141">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c3928-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3928-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3928-142">-Confirm</span></span>
<span data-ttu-id="c3928-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3928-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3928-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3928-144">-WhatIf</span></span>
<span data-ttu-id="c3928-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3928-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3928-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c3928-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3928-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3928-147">CommonParameters</span></span>
<span data-ttu-id="c3928-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3928-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3928-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3928-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3928-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3928-150">INPUTS</span></span>

### <span data-ttu-id="c3928-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c3928-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c3928-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c3928-152">OUTPUTS</span></span>

### <span data-ttu-id="c3928-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="c3928-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="c3928-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c3928-154">NOTES</span></span>

## <span data-ttu-id="c3928-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3928-155">RELATED LINKS</span></span>
