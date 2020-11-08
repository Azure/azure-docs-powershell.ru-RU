---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247989"
---
# <span data-ttu-id="b658a-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="b658a-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="b658a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b658a-102">SYNOPSIS</span></span>
<span data-ttu-id="b658a-103">Обновляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="b658a-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="b658a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b658a-104">SYNTAX</span></span>

### <span data-ttu-id="b658a-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b658a-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b658a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b658a-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b658a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b658a-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b658a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b658a-108">DESCRIPTION</span></span>
<span data-ttu-id="b658a-109">Командлет Update-AzSqlVMGroup обновляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="b658a-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="b658a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b658a-110">EXAMPLES</span></span>

### <span data-ttu-id="b658a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b658a-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="b658a-112">Обновляет Теги группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="b658a-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="b658a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b658a-113">PARAMETERS</span></span>

### <span data-ttu-id="b658a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b658a-114">-AsJob</span></span>
<span data-ttu-id="b658a-115">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="b658a-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b658a-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="b658a-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="b658a-117">Имя, используемое для создания кластера</span><span class="sxs-lookup"><span data-stu-id="b658a-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="b658a-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="b658a-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="b658a-119">Имя, используемое для работы с кластером</span><span class="sxs-lookup"><span data-stu-id="b658a-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="b658a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b658a-120">-DefaultProfile</span></span>
<span data-ttu-id="b658a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b658a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b658a-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="b658a-122">-DomainFqdn</span></span>
<span data-ttu-id="b658a-123">Полное доменное имя домена</span><span class="sxs-lookup"><span data-stu-id="b658a-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="b658a-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="b658a-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="b658a-125">Необязательный путь для следящего сервера</span><span class="sxs-lookup"><span data-stu-id="b658a-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="b658a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b658a-126">-InputObject</span></span>
<span data-ttu-id="b658a-127">Объект виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="b658a-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="b658a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b658a-128">-Name</span></span>
<span data-ttu-id="b658a-129">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="b658a-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="b658a-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="b658a-130">-OuPath</span></span>
<span data-ttu-id="b658a-131">Путь к организационному подразделению, в котором будут представлены узлы и кластер</span><span class="sxs-lookup"><span data-stu-id="b658a-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="b658a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b658a-132">-ResourceGroupName</span></span>
<span data-ttu-id="b658a-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b658a-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="b658a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b658a-134">-ResourceId</span></span>
<span data-ttu-id="b658a-135">Идентификатор ресурса группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="b658a-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="b658a-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="b658a-136">-SqlServiceAccount</span></span>
<span data-ttu-id="b658a-137">Имя, под которым служба SQL будет работать на всех виртуальных машинах SQL, участвующих в кластере.</span><span class="sxs-lookup"><span data-stu-id="b658a-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="b658a-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b658a-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="b658a-139">Первичный ключ учетной записи хранения следящего сервера</span><span class="sxs-lookup"><span data-stu-id="b658a-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="b658a-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b658a-140">-StorageAccountUrl</span></span>
<span data-ttu-id="b658a-141">Первичный ключ учетной записи хранения следящего сервера</span><span class="sxs-lookup"><span data-stu-id="b658a-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="b658a-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="b658a-142">-Tag</span></span>
<span data-ttu-id="b658a-143">Теги, связываемые с группой виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="b658a-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="b658a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b658a-144">-Confirm</span></span>
<span data-ttu-id="b658a-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b658a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b658a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b658a-146">-WhatIf</span></span>
<span data-ttu-id="b658a-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b658a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b658a-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b658a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b658a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b658a-149">CommonParameters</span></span>
<span data-ttu-id="b658a-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b658a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b658a-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b658a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b658a-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b658a-152">INPUTS</span></span>

### <span data-ttu-id="b658a-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b658a-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="b658a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b658a-154">System.String</span></span>

## <span data-ttu-id="b658a-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b658a-155">OUTPUTS</span></span>

### <span data-ttu-id="b658a-156">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b658a-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b658a-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="b658a-157">NOTES</span></span>

## <span data-ttu-id="b658a-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b658a-158">RELATED LINKS</span></span>
