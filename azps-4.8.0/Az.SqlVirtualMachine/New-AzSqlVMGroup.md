---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235269"
---
# <span data-ttu-id="2135b-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="2135b-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="2135b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2135b-102">SYNOPSIS</span></span>
<span data-ttu-id="2135b-103">Создание новой группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="2135b-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="2135b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2135b-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2135b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2135b-105">DESCRIPTION</span></span>
<span data-ttu-id="2135b-106">Командлет New-AzSqlVMGroup создает группу виртуальных машин Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2135b-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="2135b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2135b-107">EXAMPLES</span></span>

### <span data-ttu-id="2135b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2135b-108">Example 1</span></span>
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

<span data-ttu-id="2135b-109">Создание новой группы виртуальных машин SQL Azure с помощью виртуальной машины группы тестов в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2135b-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="2135b-110">$profile является объектом типа Microsoft. Azure. Management. SqlVirtualMachine. Models. WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="2135b-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="2135b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2135b-111">PARAMETERS</span></span>

### <span data-ttu-id="2135b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2135b-112">-AsJob</span></span>
<span data-ttu-id="2135b-113">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="2135b-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2135b-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="2135b-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="2135b-115">Имя, используемое для создания кластера</span><span class="sxs-lookup"><span data-stu-id="2135b-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="2135b-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="2135b-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="2135b-117">Имя, используемое для работы с кластером</span><span class="sxs-lookup"><span data-stu-id="2135b-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="2135b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2135b-118">-DefaultProfile</span></span>
<span data-ttu-id="2135b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2135b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2135b-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="2135b-120">-DomainFqdn</span></span>
<span data-ttu-id="2135b-121">Полное доменное имя домена</span><span class="sxs-lookup"><span data-stu-id="2135b-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="2135b-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="2135b-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="2135b-123">Необязательный путь для следящего сервера</span><span class="sxs-lookup"><span data-stu-id="2135b-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="2135b-124">-Location</span><span class="sxs-lookup"><span data-stu-id="2135b-124">-Location</span></span>
<span data-ttu-id="2135b-125">Расположение группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="2135b-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="2135b-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2135b-126">-Name</span></span>
<span data-ttu-id="2135b-127">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="2135b-127">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="2135b-128">-Предложение</span><span class="sxs-lookup"><span data-stu-id="2135b-128">-Offer</span></span>
<span data-ttu-id="2135b-129">Предложение группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="2135b-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="2135b-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="2135b-130">-OuPath</span></span>
<span data-ttu-id="2135b-131">Путь к организационному подразделению, в котором будут представлены узлы и кластер</span><span class="sxs-lookup"><span data-stu-id="2135b-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="2135b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2135b-132">-ResourceGroupName</span></span>
<span data-ttu-id="2135b-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2135b-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="2135b-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="2135b-134">-Sku</span></span>
<span data-ttu-id="2135b-135">Тип выпуска группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="2135b-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="2135b-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="2135b-136">-SqlServiceAccount</span></span>
<span data-ttu-id="2135b-137">Имя, под которым служба SQL будет работать на всех виртуальных машинах SQL, участвующих в кластере.</span><span class="sxs-lookup"><span data-stu-id="2135b-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="2135b-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="2135b-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="2135b-139">Первичный ключ учетной записи хранения следящего сервера</span><span class="sxs-lookup"><span data-stu-id="2135b-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="2135b-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="2135b-140">-StorageAccountUrl</span></span>
<span data-ttu-id="2135b-141">Первичный ключ учетной записи хранения следящего сервера</span><span class="sxs-lookup"><span data-stu-id="2135b-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="2135b-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="2135b-142">-Tag</span></span>
<span data-ttu-id="2135b-143">Теги, связываемые с группой виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="2135b-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="2135b-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2135b-144">-Confirm</span></span>
<span data-ttu-id="2135b-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2135b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2135b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2135b-146">-WhatIf</span></span>
<span data-ttu-id="2135b-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2135b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2135b-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2135b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2135b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2135b-149">CommonParameters</span></span>
<span data-ttu-id="2135b-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2135b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2135b-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2135b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2135b-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2135b-152">INPUTS</span></span>

### <span data-ttu-id="2135b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2135b-153">System.String</span></span>

## <span data-ttu-id="2135b-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2135b-154">OUTPUTS</span></span>

### <span data-ttu-id="2135b-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="2135b-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="2135b-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="2135b-156">NOTES</span></span>

## <span data-ttu-id="2135b-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2135b-157">RELATED LINKS</span></span>
