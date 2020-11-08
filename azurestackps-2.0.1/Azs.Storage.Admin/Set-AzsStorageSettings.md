---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2020
ms.locfileid: "94075389"
---
# <span data-ttu-id="3fb38-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="3fb38-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="3fb38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fb38-102">SYNOPSIS</span></span>


## <span data-ttu-id="3fb38-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fb38-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3fb38-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fb38-104">DESCRIPTION</span></span>


## <span data-ttu-id="3fb38-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fb38-105">EXAMPLES</span></span>

### <span data-ttu-id="3fb38-106">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="3fb38-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="3fb38-107">Обновите параметры хранилища.</span><span class="sxs-lookup"><span data-stu-id="3fb38-107">Update the storage settings.</span></span>

## <span data-ttu-id="3fb38-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fb38-108">PARAMETERS</span></span>

### <span data-ttu-id="3fb38-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb38-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="3fb38-110">-Force</span><span class="sxs-lookup"><span data-stu-id="3fb38-110">-Force</span></span>


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

### <span data-ttu-id="3fb38-111">-Location</span><span class="sxs-lookup"><span data-stu-id="3fb38-111">-Location</span></span>


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

### <span data-ttu-id="3fb38-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="3fb38-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3fb38-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fb38-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="3fb38-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fb38-114">-Confirm</span></span>
<span data-ttu-id="3fb38-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3fb38-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fb38-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb38-116">-WhatIf</span></span>
<span data-ttu-id="3fb38-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3fb38-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fb38-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3fb38-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fb38-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb38-119">CommonParameters</span></span>
<span data-ttu-id="3fb38-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fb38-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb38-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fb38-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb38-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fb38-122">INPUTS</span></span>

## <span data-ttu-id="3fb38-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fb38-123">OUTPUTS</span></span>

### <span data-ttu-id="3fb38-124">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="3fb38-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="3fb38-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fb38-125">NOTES</span></span>

## <span data-ttu-id="3fb38-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fb38-126">RELATED LINKS</span></span>

