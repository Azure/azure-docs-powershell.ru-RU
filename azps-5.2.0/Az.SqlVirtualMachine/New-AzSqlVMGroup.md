---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394084"
---
# <span data-ttu-id="c674c-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="c674c-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="c674c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c674c-102">SYNOPSIS</span></span>
<span data-ttu-id="c674c-103">Создает новую группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="c674c-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="c674c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c674c-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c674c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c674c-105">DESCRIPTION</span></span>
<span data-ttu-id="c674c-106">С New-AzSqlVMGroup создается группа виртуальных машин Azure SQL machine.</span><span class="sxs-lookup"><span data-stu-id="c674c-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="c674c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c674c-107">EXAMPLES</span></span>

### <span data-ttu-id="c674c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c674c-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="c674c-109">Создает новую группу виртуальных SQL Azure с test-group vm в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c674c-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="c674c-110">$profile является объектом типа Microsoft.Azure.Management.SqlVirtualMa modelse.Models.WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="c674c-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="c674c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c674c-111">PARAMETERS</span></span>

### <span data-ttu-id="c674c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c674c-112">-AsJob</span></span>
<span data-ttu-id="c674c-113">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="c674c-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c674c-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="c674c-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="c674c-115">Имя, используемая для создания кластера</span><span class="sxs-lookup"><span data-stu-id="c674c-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="c674c-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="c674c-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="c674c-117">Имя, используемая для кластера операционных систем</span><span class="sxs-lookup"><span data-stu-id="c674c-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="c674c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c674c-118">-DefaultProfile</span></span>
<span data-ttu-id="c674c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c674c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c674c-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="c674c-120">-DomainFqdn</span></span>
<span data-ttu-id="c674c-121">Полное имя домена</span><span class="sxs-lookup"><span data-stu-id="c674c-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="c674c-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="c674c-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="c674c-123">Необязательный путь для fileshare</span><span class="sxs-lookup"><span data-stu-id="c674c-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="c674c-124">-Location</span><span class="sxs-lookup"><span data-stu-id="c674c-124">-Location</span></span>
<span data-ttu-id="c674c-125">SQL расположение группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c674c-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c674c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c674c-126">-Name</span></span>
<span data-ttu-id="c674c-127">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c674c-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c674c-128">-Offer</span><span class="sxs-lookup"><span data-stu-id="c674c-128">-Offer</span></span>
<span data-ttu-id="c674c-129">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c674c-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="c674c-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="c674c-130">-OuPath</span></span>
<span data-ttu-id="c674c-131">Путь к подразделению, в котором будут присутствовать узлы и кластер</span><span class="sxs-lookup"><span data-stu-id="c674c-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="c674c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c674c-132">-ResourceGroupName</span></span>
<span data-ttu-id="c674c-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c674c-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c674c-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="c674c-134">-Sku</span></span>
<span data-ttu-id="c674c-135">SQL выпуска группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c674c-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="c674c-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="c674c-136">-SqlServiceAccount</span></span>
<span data-ttu-id="c674c-137">Имя, под SQL службы будут работать на всех SQL виртуальных машинах в кластере.</span><span class="sxs-lookup"><span data-stu-id="c674c-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="c674c-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c674c-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="c674c-139">Первичный ключ учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c674c-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c674c-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="c674c-140">-StorageAccountUrl</span></span>
<span data-ttu-id="c674c-141">Первичный ключ учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c674c-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="c674c-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="c674c-142">-Tag</span></span>
<span data-ttu-id="c674c-143">Теги, которые нужно связать с группой SQL машин.</span><span class="sxs-lookup"><span data-stu-id="c674c-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="c674c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c674c-144">-Confirm</span></span>
<span data-ttu-id="c674c-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c674c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c674c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c674c-146">-WhatIf</span></span>
<span data-ttu-id="c674c-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c674c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c674c-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c674c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c674c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c674c-149">CommonParameters</span></span>
<span data-ttu-id="c674c-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c674c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c674c-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c674c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c674c-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c674c-152">INPUTS</span></span>

### <span data-ttu-id="c674c-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c674c-153">System.String</span></span>

## <span data-ttu-id="c674c-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c674c-154">OUTPUTS</span></span>

### <span data-ttu-id="c674c-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="c674c-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="c674c-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c674c-156">NOTES</span></span>

## <span data-ttu-id="c674c-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c674c-157">RELATED LINKS</span></span>
