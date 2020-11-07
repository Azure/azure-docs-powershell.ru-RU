---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910474"
---
# <span data-ttu-id="27623-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="27623-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="27623-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27623-102">SYNOPSIS</span></span>


## <span data-ttu-id="27623-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27623-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27623-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27623-104">DESCRIPTION</span></span>


## <span data-ttu-id="27623-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27623-105">EXAMPLES</span></span>

### <span data-ttu-id="27623-106">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="27623-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="27623-107">Начните сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="27623-107">Start garbage collection.</span></span>

## <span data-ttu-id="27623-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27623-108">PARAMETERS</span></span>

### <span data-ttu-id="27623-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27623-109">-AsJob</span></span>


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

### <span data-ttu-id="27623-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27623-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="27623-111">-Force</span><span class="sxs-lookup"><span data-stu-id="27623-111">-Force</span></span>


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

### <span data-ttu-id="27623-112">-Location</span><span class="sxs-lookup"><span data-stu-id="27623-112">-Location</span></span>


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

### <span data-ttu-id="27623-113">-Wait</span><span class="sxs-lookup"><span data-stu-id="27623-113">-NoWait</span></span>


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

### <span data-ttu-id="27623-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27623-114">-PassThru</span></span>


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

### <span data-ttu-id="27623-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27623-115">-SubscriptionId</span></span>


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

### <span data-ttu-id="27623-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27623-116">-Confirm</span></span>
<span data-ttu-id="27623-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27623-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27623-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27623-118">-WhatIf</span></span>
<span data-ttu-id="27623-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27623-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27623-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27623-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27623-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27623-121">CommonParameters</span></span>
<span data-ttu-id="27623-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27623-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27623-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27623-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27623-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27623-124">INPUTS</span></span>

## <span data-ttu-id="27623-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27623-125">OUTPUTS</span></span>

### <span data-ttu-id="27623-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27623-126">System.Boolean</span></span>



## <span data-ttu-id="27623-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="27623-127">NOTES</span></span>

## <span data-ttu-id="27623-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27623-128">RELATED LINKS</span></span>

