---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065542"
---
# <span data-ttu-id="75019-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="75019-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="75019-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75019-102">SYNOPSIS</span></span>
<span data-ttu-id="75019-103">Обновляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="75019-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="75019-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75019-104">SYNTAX</span></span>

### <span data-ttu-id="75019-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75019-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75019-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="75019-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75019-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="75019-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75019-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75019-108">DESCRIPTION</span></span>
<span data-ttu-id="75019-109">Командлет Update-AzSqlVMGroup обновляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="75019-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="75019-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75019-110">EXAMPLES</span></span>

### <span data-ttu-id="75019-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75019-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="75019-112">Обновляет Теги группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="75019-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="75019-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75019-113">PARAMETERS</span></span>

### <span data-ttu-id="75019-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75019-114">-AsJob</span></span>
<span data-ttu-id="75019-115">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="75019-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="75019-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="75019-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="75019-117">Имя, используемое для создания кластера</span><span class="sxs-lookup"><span data-stu-id="75019-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="75019-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="75019-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="75019-119">Имя, используемое для работы с кластером</span><span class="sxs-lookup"><span data-stu-id="75019-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="75019-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75019-120">-DefaultProfile</span></span>
<span data-ttu-id="75019-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75019-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75019-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="75019-122">-DomainFqdn</span></span>
<span data-ttu-id="75019-123">Полное доменное имя домена</span><span class="sxs-lookup"><span data-stu-id="75019-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="75019-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="75019-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="75019-125">Необязательный путь для следящего сервера</span><span class="sxs-lookup"><span data-stu-id="75019-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="75019-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75019-126">-InputObject</span></span>
<span data-ttu-id="75019-127">Объект виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="75019-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="75019-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75019-128">-Name</span></span>
<span data-ttu-id="75019-129">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="75019-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="75019-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="75019-130">-OuPath</span></span>
<span data-ttu-id="75019-131">Путь к организационному подразделению, в котором будут представлены узлы и кластер</span><span class="sxs-lookup"><span data-stu-id="75019-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="75019-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75019-132">-ResourceGroupName</span></span>
<span data-ttu-id="75019-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75019-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="75019-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75019-134">-ResourceId</span></span>
<span data-ttu-id="75019-135">Идентификатор ресурса группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="75019-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="75019-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="75019-136">-SqlServiceAccount</span></span>
<span data-ttu-id="75019-137">Имя, под которым служба SQL будет работать на всех виртуальных машинах SQL, участвующих в кластере.</span><span class="sxs-lookup"><span data-stu-id="75019-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="75019-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="75019-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="75019-139">Первичный ключ учетной записи хранения следящего сервера</span><span class="sxs-lookup"><span data-stu-id="75019-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="75019-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="75019-140">-StorageAccountUrl</span></span>
<span data-ttu-id="75019-141">Первичный ключ учетной записи хранения следящего сервера</span><span class="sxs-lookup"><span data-stu-id="75019-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="75019-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="75019-142">-Tag</span></span>
<span data-ttu-id="75019-143">Теги, связываемые с группой виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="75019-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="75019-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75019-144">-Confirm</span></span>
<span data-ttu-id="75019-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75019-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75019-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75019-146">-WhatIf</span></span>
<span data-ttu-id="75019-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75019-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75019-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75019-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75019-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75019-149">CommonParameters</span></span>
<span data-ttu-id="75019-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75019-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75019-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75019-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75019-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75019-152">INPUTS</span></span>

### <span data-ttu-id="75019-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="75019-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="75019-154">System. String</span><span class="sxs-lookup"><span data-stu-id="75019-154">System.String</span></span>

## <span data-ttu-id="75019-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75019-155">OUTPUTS</span></span>

### <span data-ttu-id="75019-156">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="75019-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="75019-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="75019-157">NOTES</span></span>

## <span data-ttu-id="75019-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75019-158">RELATED LINKS</span></span>
