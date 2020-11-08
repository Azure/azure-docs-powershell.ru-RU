---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076606"
---
# <span data-ttu-id="0d934-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="0d934-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="0d934-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d934-102">SYNOPSIS</span></span>


## <span data-ttu-id="0d934-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d934-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d934-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d934-104">DESCRIPTION</span></span>


## <span data-ttu-id="0d934-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d934-105">EXAMPLES</span></span>

### <span data-ttu-id="0d934-106">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="0d934-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="0d934-107">Начните сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="0d934-107">Start garbage collection.</span></span>

## <span data-ttu-id="0d934-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d934-108">PARAMETERS</span></span>

### <span data-ttu-id="0d934-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d934-109">-AsJob</span></span>


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

### <span data-ttu-id="0d934-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d934-110">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0d934-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0d934-111">-Force</span></span>


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

### <span data-ttu-id="0d934-112">-Location</span><span class="sxs-lookup"><span data-stu-id="0d934-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0d934-113">-Wait</span><span class="sxs-lookup"><span data-stu-id="0d934-113">-NoWait</span></span>


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

### <span data-ttu-id="0d934-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d934-114">-PassThru</span></span>


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

### <span data-ttu-id="0d934-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d934-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0d934-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d934-116">-Confirm</span></span>
<span data-ttu-id="0d934-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d934-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d934-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d934-118">-WhatIf</span></span>
<span data-ttu-id="0d934-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d934-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d934-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d934-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d934-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d934-121">CommonParameters</span></span>
<span data-ttu-id="0d934-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d934-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d934-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d934-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d934-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d934-124">INPUTS</span></span>

## <span data-ttu-id="0d934-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d934-125">OUTPUTS</span></span>

### <span data-ttu-id="0d934-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d934-126">System.Boolean</span></span>



## <span data-ttu-id="0d934-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d934-127">NOTES</span></span>

## <span data-ttu-id="0d934-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d934-128">RELATED LINKS</span></span>

