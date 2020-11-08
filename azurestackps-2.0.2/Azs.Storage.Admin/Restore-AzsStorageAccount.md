---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077009"
---
# <span data-ttu-id="8e327-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e327-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="8e327-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e327-102">SYNOPSIS</span></span>


## <span data-ttu-id="8e327-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e327-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e327-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e327-104">DESCRIPTION</span></span>


## <span data-ttu-id="8e327-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e327-105">EXAMPLES</span></span>

### <span data-ttu-id="8e327-106">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="8e327-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="8e327-107">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8e327-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="8e327-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e327-108">PARAMETERS</span></span>

### <span data-ttu-id="8e327-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e327-109">-AsJob</span></span>


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

### <span data-ttu-id="8e327-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e327-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="8e327-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8e327-111">-Force</span></span>


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

### <span data-ttu-id="8e327-112">-Location</span><span class="sxs-lookup"><span data-stu-id="8e327-112">-Location</span></span>


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

### <span data-ttu-id="8e327-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e327-113">-Name</span></span>


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

### <span data-ttu-id="8e327-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="8e327-114">-NewAccountName</span></span>


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

### <span data-ttu-id="8e327-115">-Wait</span><span class="sxs-lookup"><span data-stu-id="8e327-115">-NoWait</span></span>


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

### <span data-ttu-id="8e327-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e327-116">-PassThru</span></span>


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

### <span data-ttu-id="8e327-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e327-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="8e327-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e327-118">-Confirm</span></span>
<span data-ttu-id="8e327-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e327-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e327-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e327-120">-WhatIf</span></span>
<span data-ttu-id="8e327-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e327-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e327-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e327-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e327-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e327-123">CommonParameters</span></span>
<span data-ttu-id="8e327-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e327-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e327-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e327-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e327-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e327-126">INPUTS</span></span>

## <span data-ttu-id="8e327-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e327-127">OUTPUTS</span></span>

### <span data-ttu-id="8e327-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e327-128">System.Boolean</span></span>



## <span data-ttu-id="8e327-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e327-129">NOTES</span></span>

## <span data-ttu-id="8e327-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e327-130">RELATED LINKS</span></span>

