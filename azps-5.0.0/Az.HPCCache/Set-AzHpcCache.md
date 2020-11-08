---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247394"
---
# <span data-ttu-id="c3156-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="c3156-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="c3156-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3156-102">SYNOPSIS</span></span>
<span data-ttu-id="c3156-103">Обновляет теги в кэше HPC.</span><span class="sxs-lookup"><span data-stu-id="c3156-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="c3156-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3156-104">SYNTAX</span></span>

### <span data-ttu-id="c3156-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3156-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3156-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3156-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3156-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3156-107">DESCRIPTION</span></span>
<span data-ttu-id="c3156-108">Командлет **Set-AzHpcCache** обновляет Теги кэша Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="c3156-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="c3156-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3156-109">EXAMPLES</span></span>

### <span data-ttu-id="c3156-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3156-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="c3156-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3156-111">PARAMETERS</span></span>

### <span data-ttu-id="c3156-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3156-112">-AsJob</span></span>
<span data-ttu-id="c3156-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c3156-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3156-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3156-114">-DefaultProfile</span></span>
<span data-ttu-id="c3156-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3156-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3156-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3156-116">-InputObject</span></span>
<span data-ttu-id="c3156-117">Обновляемый объект кэша.</span><span class="sxs-lookup"><span data-stu-id="c3156-117">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3156-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3156-118">-Name</span></span>
<span data-ttu-id="c3156-119">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="c3156-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3156-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3156-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3156-121">Имя группы ресурсов, в которой вы хотите обновить кэш.</span><span class="sxs-lookup"><span data-stu-id="c3156-121">Name of resource group under which you want to update cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3156-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="c3156-122">-Tag</span></span>
<span data-ttu-id="c3156-123">Теги, которые нужно связать с кэшем HPC.</span><span class="sxs-lookup"><span data-stu-id="c3156-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3156-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3156-124">-Confirm</span></span>
<span data-ttu-id="c3156-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c3156-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3156-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3156-126">-WhatIf</span></span>
<span data-ttu-id="c3156-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c3156-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3156-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c3156-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3156-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3156-129">CommonParameters</span></span>
<span data-ttu-id="c3156-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3156-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3156-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3156-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3156-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3156-132">INPUTS</span></span>

### <span data-ttu-id="c3156-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c3156-133">System.String</span></span>

### <span data-ttu-id="c3156-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c3156-134">System.Int32</span></span>

## <span data-ttu-id="c3156-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3156-135">OUTPUTS</span></span>

### <span data-ttu-id="c3156-136">Microsoft. Azure. PowerShell. командлеты. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="c3156-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="c3156-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3156-137">NOTES</span></span>

## <span data-ttu-id="c3156-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3156-138">RELATED LINKS</span></span>
