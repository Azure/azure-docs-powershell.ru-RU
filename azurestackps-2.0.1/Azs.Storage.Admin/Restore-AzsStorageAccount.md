---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2020
ms.locfileid: "94075387"
---
# <span data-ttu-id="a968d-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a968d-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="a968d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a968d-102">SYNOPSIS</span></span>


## <span data-ttu-id="a968d-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a968d-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a968d-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a968d-104">DESCRIPTION</span></span>


## <span data-ttu-id="a968d-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a968d-105">EXAMPLES</span></span>

### <span data-ttu-id="a968d-106">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="a968d-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="a968d-107">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a968d-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="a968d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a968d-108">PARAMETERS</span></span>

### <span data-ttu-id="a968d-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a968d-109">-AsJob</span></span>


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

### <span data-ttu-id="a968d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a968d-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="a968d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a968d-111">-Force</span></span>


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

### <span data-ttu-id="a968d-112">-Location</span><span class="sxs-lookup"><span data-stu-id="a968d-112">-Location</span></span>


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

### <span data-ttu-id="a968d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a968d-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a968d-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="a968d-114">-NewAccountName</span></span>


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

### <span data-ttu-id="a968d-115">-Wait</span><span class="sxs-lookup"><span data-stu-id="a968d-115">-NoWait</span></span>


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

### <span data-ttu-id="a968d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a968d-116">-PassThru</span></span>


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

### <span data-ttu-id="a968d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a968d-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="a968d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a968d-118">-Confirm</span></span>
<span data-ttu-id="a968d-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a968d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a968d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a968d-120">-WhatIf</span></span>
<span data-ttu-id="a968d-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a968d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a968d-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a968d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a968d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a968d-123">CommonParameters</span></span>
<span data-ttu-id="a968d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a968d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a968d-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a968d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a968d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a968d-126">INPUTS</span></span>

## <span data-ttu-id="a968d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a968d-127">OUTPUTS</span></span>

### <span data-ttu-id="a968d-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a968d-128">System.Boolean</span></span>



## <span data-ttu-id="a968d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a968d-129">NOTES</span></span>

## <span data-ttu-id="a968d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a968d-130">RELATED LINKS</span></span>

