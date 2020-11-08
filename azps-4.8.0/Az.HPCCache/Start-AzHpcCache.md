---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244939"
---
# <span data-ttu-id="36be1-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="36be1-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="36be1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36be1-102">SYNOPSIS</span></span>
<span data-ttu-id="36be1-103">Запускает кэш HPC.</span><span class="sxs-lookup"><span data-stu-id="36be1-103">Starts HPC cache.</span></span>

## <span data-ttu-id="36be1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36be1-104">SYNTAX</span></span>

### <span data-ttu-id="36be1-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36be1-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36be1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36be1-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36be1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36be1-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36be1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36be1-108">DESCRIPTION</span></span>
<span data-ttu-id="36be1-109">Командлет **Start-AzHpcCache** запускает кэш Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="36be1-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="36be1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36be1-110">EXAMPLES</span></span>

### <span data-ttu-id="36be1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36be1-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="36be1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36be1-112">PARAMETERS</span></span>

### <span data-ttu-id="36be1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36be1-113">-AsJob</span></span>
<span data-ttu-id="36be1-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="36be1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36be1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36be1-115">-DefaultProfile</span></span>
<span data-ttu-id="36be1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36be1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36be1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="36be1-117">-Force</span></span>
<span data-ttu-id="36be1-118">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="36be1-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="36be1-119">По умолчанию этот командлет предлагает подтвердить необходимость запуска кэша.</span><span class="sxs-lookup"><span data-stu-id="36be1-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="36be1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36be1-120">-InputObject</span></span>
<span data-ttu-id="36be1-121">Объект кэша, который нужно запустить.</span><span class="sxs-lookup"><span data-stu-id="36be1-121">The cache object to start.</span></span>

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

### <span data-ttu-id="36be1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36be1-122">-Name</span></span>
<span data-ttu-id="36be1-123">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="36be1-123">Name of cache.</span></span>

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

### <span data-ttu-id="36be1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36be1-124">-PassThru</span></span>
<span data-ttu-id="36be1-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="36be1-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36be1-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36be1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="36be1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36be1-127">-ResourceGroupName</span></span>
<span data-ttu-id="36be1-128">Имя группы ресурсов, в которой вы хотите запустить кэширование.</span><span class="sxs-lookup"><span data-stu-id="36be1-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="36be1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36be1-129">-ResourceId</span></span>
<span data-ttu-id="36be1-130">Идентификатор ресурса кэша</span><span class="sxs-lookup"><span data-stu-id="36be1-130">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36be1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36be1-131">-Confirm</span></span>
<span data-ttu-id="36be1-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36be1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36be1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36be1-133">-WhatIf</span></span>
<span data-ttu-id="36be1-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36be1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36be1-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36be1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36be1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36be1-136">CommonParameters</span></span>
<span data-ttu-id="36be1-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36be1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36be1-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36be1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36be1-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36be1-139">INPUTS</span></span>

### <span data-ttu-id="36be1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="36be1-140">System.String</span></span>

## <span data-ttu-id="36be1-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36be1-141">OUTPUTS</span></span>

## <span data-ttu-id="36be1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="36be1-142">NOTES</span></span>

## <span data-ttu-id="36be1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36be1-143">RELATED LINKS</span></span>
