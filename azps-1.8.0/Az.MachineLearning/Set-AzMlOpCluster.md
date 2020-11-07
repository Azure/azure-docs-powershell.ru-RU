---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/set-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
ms.openlocfilehash: 833b3456cd39e4589ceaf37e0c86fd654c250ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899733"
---
# <span data-ttu-id="5c1dd-101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5c1dd-101">Set-AzMlOpCluster</span></span>

## <span data-ttu-id="5c1dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1dd-103">Задает свойства кластера операций.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-103">Sets the properties of an operationalization cluster.</span></span>

## <span data-ttu-id="5c1dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c1dd-104">SYNTAX</span></span>

### <span data-ttu-id="5c1dd-105">SetByIndividualParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c1dd-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1dd-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="5c1dd-106">SetByInputObject</span></span>
```
Set-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1dd-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c1dd-107">SetByResourceId</span></span>
```
Set-AzMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>] [-SslCertificate <String>]
 [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c1dd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c1dd-108">DESCRIPTION</span></span>
<span data-ttu-id="5c1dd-109">Задает все свойства кластера операций.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="5c1dd-110">Так как при использовании объекта кластера устанавливаются все свойства, необходимо передать полный допустимый объект ввода.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="5c1dd-111">Свойства, предназначенные только для чтения, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="5c1dd-112">В настоящее время поддерживается обновление только некоторых свойств, как показано в наборах параметров.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="5c1dd-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c1dd-113">EXAMPLES</span></span>

### <span data-ttu-id="5c1dd-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5c1dd-114">Example 1</span></span>
<span data-ttu-id="5c1dd-115">Обновление кластера с использованием отдельных параметров.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="5c1dd-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5c1dd-116">Example 2</span></span>
<span data-ttu-id="5c1dd-117">Обновите кластер с помощью объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="5c1dd-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c1dd-118">PARAMETERS</span></span>

### <span data-ttu-id="5c1dd-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="5c1dd-119">-AgentCount</span></span>
<span data-ttu-id="5c1dd-120">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1dd-121">-DefaultProfile</span></span>
<span data-ttu-id="5c1dd-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c1dd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c1dd-123">-InputObject</span></span>
<span data-ttu-id="5c1dd-124">Свойства кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c1dd-125">-Name</span></span>
<span data-ttu-id="5c1dd-126">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c1dd-128">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c1dd-129">-ResourceId</span></span>
<span data-ttu-id="5c1dd-130">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="5c1dd-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c1dd-131">-SslCertificate</span></span>
<span data-ttu-id="5c1dd-132">Данные сертификата SSL в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="5c1dd-133">-SslCName</span></span>
<span data-ttu-id="5c1dd-134">CName-запись сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="5c1dd-135">-SslKey</span></span>
<span data-ttu-id="5c1dd-136">Данные ключа SSL в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="5c1dd-137">-SslStatus</span></span>
<span data-ttu-id="5c1dd-138">Состояние SSL.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-138">SSL status.</span></span>
<span data-ttu-id="5c1dd-139">Возможны значения "включено" и "отключено".</span><span class="sxs-lookup"><span data-stu-id="5c1dd-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1dd-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c1dd-140">-Confirm</span></span>
<span data-ttu-id="5c1dd-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1dd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1dd-142">-WhatIf</span></span>
<span data-ttu-id="5c1dd-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c1dd-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1dd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1dd-145">CommonParameters</span></span>
<span data-ttu-id="5c1dd-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c1dd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1dd-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1dd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1dd-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c1dd-148">INPUTS</span></span>

### <span data-ttu-id="5c1dd-149">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="5c1dd-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="5c1dd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5c1dd-150">System.String</span></span>

### <span data-ttu-id="5c1dd-151">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5c1dd-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5c1dd-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c1dd-152">OUTPUTS</span></span>

### <span data-ttu-id="5c1dd-153">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="5c1dd-153">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="5c1dd-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c1dd-154">NOTES</span></span>

## <span data-ttu-id="5c1dd-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c1dd-155">RELATED LINKS</span></span>
