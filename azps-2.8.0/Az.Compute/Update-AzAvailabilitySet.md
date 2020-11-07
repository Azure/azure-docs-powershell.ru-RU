---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: ebb6635cd593e37eedf4a8e70230cbf0f42e0d92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721639"
---
# <span data-ttu-id="d18b8-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d18b8-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="d18b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d18b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d18b8-103">Обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="d18b8-103">Updates an availability set.</span></span>

## <span data-ttu-id="d18b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d18b8-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d18b8-105">DESCRIPTION</span></span>
<span data-ttu-id="d18b8-106">Командлет **Update-AzAvailabilitySet** обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="d18b8-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="d18b8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d18b8-107">EXAMPLES</span></span>

### <span data-ttu-id="d18b8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d18b8-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="d18b8-109">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов с именем "ResourceGroup01" в управляемый набор доступности.</span><span class="sxs-lookup"><span data-stu-id="d18b8-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="d18b8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d18b8-110">PARAMETERS</span></span>

### <span data-ttu-id="d18b8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d18b8-111">-AsJob</span></span>
<span data-ttu-id="d18b8-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="d18b8-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d18b8-113">-Группа доступности</span><span class="sxs-lookup"><span data-stu-id="d18b8-113">-AvailabilitySet</span></span>
<span data-ttu-id="d18b8-114">Указывает объект группы доступности, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="d18b8-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d18b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18b8-115">-DefaultProfile</span></span>
<span data-ttu-id="d18b8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d18b8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d18b8-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="d18b8-117">-Sku</span></span>
<span data-ttu-id="d18b8-118">Название SKU</span><span class="sxs-lookup"><span data-stu-id="d18b8-118">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18b8-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="d18b8-119">-Tag</span></span>
<span data-ttu-id="d18b8-120">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="d18b8-120">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="d18b8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d18b8-121">-Confirm</span></span>
<span data-ttu-id="d18b8-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d18b8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18b8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18b8-123">-WhatIf</span></span>
<span data-ttu-id="d18b8-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d18b8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d18b8-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d18b8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18b8-126">CommonParameters</span></span>
<span data-ttu-id="d18b8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d18b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18b8-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d18b8-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18b8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d18b8-129">INPUTS</span></span>

### <span data-ttu-id="d18b8-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d18b8-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d18b8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d18b8-131">OUTPUTS</span></span>

### <span data-ttu-id="d18b8-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d18b8-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d18b8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d18b8-133">NOTES</span></span>

## <span data-ttu-id="d18b8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d18b8-134">RELATED LINKS</span></span>
