---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 1843322f702f8c43f97f1cf64c9d9f5b92d419bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567032"
---
# <span data-ttu-id="ebdd0-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="ebdd0-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="ebdd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebdd0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebdd0-103">Удаление управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebdd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebdd0-104">SYNTAX</span></span>

### <span data-ttu-id="ebdd0-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebdd0-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebdd0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebdd0-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebdd0-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebdd0-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebdd0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebdd0-108">DESCRIPTION</span></span>
<span data-ttu-id="ebdd0-109">Удаление управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ebdd0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebdd0-110">EXAMPLES</span></span>

### <span data-ttu-id="ebdd0-111">Удаление существующего управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ebdd0-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="ebdd0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebdd0-112">PARAMETERS</span></span>

### <span data-ttu-id="ebdd0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebdd0-113">-AsJob</span></span>
<span data-ttu-id="ebdd0-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ebdd0-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebdd0-115">-DefaultProfile</span></span>
<span data-ttu-id="ebdd0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ebdd0-117">-Force</span></span>
<span data-ttu-id="ebdd0-118">Удаление управляемого кластера Kubernetes без запроса</span><span class="sxs-lookup"><span data-stu-id="ebdd0-118">Remove managed Kubernetes cluster without prompt</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ebdd0-119">-Id</span></span>
<span data-ttu-id="ebdd0-120">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ebdd0-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebdd0-121">-InputObject</span></span>
<span data-ttu-id="ebdd0-122">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebdd0-123">-Name</span></span>
<span data-ttu-id="ebdd0-124">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ebdd0-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebdd0-125">-PassThru</span></span>
<span data-ttu-id="ebdd0-126">Возвращает значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-126">Returns true if deletion is successful</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebdd0-127">-ResourceGroupName</span></span>
<span data-ttu-id="ebdd0-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ebdd0-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebdd0-129">-Confirm</span></span>
<span data-ttu-id="ebdd0-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebdd0-131">-WhatIf</span></span>
<span data-ttu-id="ebdd0-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebdd0-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdd0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebdd0-134">CommonParameters</span></span>
<span data-ttu-id="ebdd0-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebdd0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebdd0-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebdd0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebdd0-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebdd0-137">INPUTS</span></span>

### <span data-ttu-id="ebdd0-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ebdd0-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="ebdd0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ebdd0-139">System.String</span></span>

## <span data-ttu-id="ebdd0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebdd0-140">OUTPUTS</span></span>

### <span data-ttu-id="ebdd0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ebdd0-141">System.Boolean</span></span>

## <span data-ttu-id="ebdd0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebdd0-142">NOTES</span></span>

## <span data-ttu-id="ebdd0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebdd0-143">RELATED LINKS</span></span>
