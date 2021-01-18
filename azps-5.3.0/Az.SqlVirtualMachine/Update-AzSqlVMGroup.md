---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518766"
---
# <span data-ttu-id="30923-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="30923-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="30923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30923-102">SYNOPSIS</span></span>
<span data-ttu-id="30923-103">Обновляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="30923-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="30923-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30923-104">SYNTAX</span></span>

### <span data-ttu-id="30923-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30923-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30923-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="30923-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30923-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="30923-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30923-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30923-108">DESCRIPTION</span></span>
<span data-ttu-id="30923-109">Новый Update-AzSqlVMGroup обновляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="30923-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="30923-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30923-110">EXAMPLES</span></span>

### <span data-ttu-id="30923-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30923-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="30923-112">Обновляет теги группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="30923-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="30923-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30923-113">PARAMETERS</span></span>

### <span data-ttu-id="30923-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30923-114">-AsJob</span></span>
<span data-ttu-id="30923-115">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="30923-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="30923-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="30923-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="30923-117">Имя, используемая для создания кластера</span><span class="sxs-lookup"><span data-stu-id="30923-117">Name used for creating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="30923-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="30923-119">Имя, используемая для кластера операционных систем</span><span class="sxs-lookup"><span data-stu-id="30923-119">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30923-120">-DefaultProfile</span></span>
<span data-ttu-id="30923-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30923-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30923-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="30923-122">-DomainFqdn</span></span>
<span data-ttu-id="30923-123">Полное имя домена</span><span class="sxs-lookup"><span data-stu-id="30923-123">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="30923-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="30923-125">Необязательный путь для fileshare</span><span class="sxs-lookup"><span data-stu-id="30923-125">Optional path for fileshare witness</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30923-126">-InputObject</span></span>
<span data-ttu-id="30923-127">SQL виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="30923-127">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30923-128">-Name</span><span class="sxs-lookup"><span data-stu-id="30923-128">-Name</span></span>
<span data-ttu-id="30923-129">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="30923-129">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="30923-130">-OuPath</span></span>
<span data-ttu-id="30923-131">Путь к подразделению, в котором будут присутствовать узлы и кластер</span><span class="sxs-lookup"><span data-stu-id="30923-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30923-132">-ResourceGroupName</span></span>
<span data-ttu-id="30923-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30923-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30923-134">-ResourceId</span></span>
<span data-ttu-id="30923-135">SQL ресурса группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="30923-135">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30923-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="30923-136">-SqlServiceAccount</span></span>
<span data-ttu-id="30923-137">Имя, под SQL службы будут работать на всех SQL виртуальных машинах в кластере.</span><span class="sxs-lookup"><span data-stu-id="30923-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="30923-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="30923-139">Первичный ключ учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="30923-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="30923-140">-StorageAccountUrl</span></span>
<span data-ttu-id="30923-141">Первичный ключ учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="30923-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="30923-142">-Tag</span></span>
<span data-ttu-id="30923-143">Теги, которые нужно связать с группой SQL машин.</span><span class="sxs-lookup"><span data-stu-id="30923-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30923-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30923-144">-Confirm</span></span>
<span data-ttu-id="30923-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30923-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30923-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30923-146">-WhatIf</span></span>
<span data-ttu-id="30923-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30923-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30923-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30923-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30923-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30923-149">CommonParameters</span></span>
<span data-ttu-id="30923-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30923-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30923-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30923-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30923-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30923-152">INPUTS</span></span>

### <span data-ttu-id="30923-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMaviree.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="30923-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="30923-154">System.String</span><span class="sxs-lookup"><span data-stu-id="30923-154">System.String</span></span>

## <span data-ttu-id="30923-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30923-155">OUTPUTS</span></span>

### <span data-ttu-id="30923-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMaviree.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="30923-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="30923-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30923-157">NOTES</span></span>

## <span data-ttu-id="30923-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30923-158">RELATED LINKS</span></span>
