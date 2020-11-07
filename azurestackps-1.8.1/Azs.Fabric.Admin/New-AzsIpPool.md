---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908805"
---
# <span data-ttu-id="430af-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="430af-101">New-AzsIpPool</span></span>

## <span data-ttu-id="430af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="430af-102">SYNOPSIS</span></span>
<span data-ttu-id="430af-103">Создание пула IP-адресов инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="430af-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="430af-104">После создания пул IP-адресов нельзя удалить или изменить.</span><span class="sxs-lookup"><span data-stu-id="430af-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="430af-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="430af-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="430af-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="430af-106">DESCRIPTION</span></span>
<span data-ttu-id="430af-107">Создание пула IP-адресов инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="430af-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="430af-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="430af-108">EXAMPLES</span></span>

### <span data-ttu-id="430af-109">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="430af-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="430af-110">Создание нового пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="430af-110">Create a new IP pool.</span></span>

## <span data-ttu-id="430af-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="430af-111">PARAMETERS</span></span>

### <span data-ttu-id="430af-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="430af-112">-Name</span></span>
<span data-ttu-id="430af-113">Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="430af-113">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430af-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="430af-114">-AddressPrefix</span></span>
<span data-ttu-id="430af-115">Префикс адреса.</span><span class="sxs-lookup"><span data-stu-id="430af-115">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430af-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="430af-116">-StartIpAddress</span></span>
<span data-ttu-id="430af-117">Начальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="430af-117">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430af-118">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="430af-118">-EndIpAddress</span></span>
<span data-ttu-id="430af-119">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="430af-119">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430af-120">-Location</span><span class="sxs-lookup"><span data-stu-id="430af-120">-Location</span></span>
<span data-ttu-id="430af-121">Область, в которой расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="430af-121">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="430af-122">-ResourceGroupName</span></span>
<span data-ttu-id="430af-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="430af-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430af-124">-Теги</span><span class="sxs-lookup"><span data-stu-id="430af-124">-Tags</span></span>
<span data-ttu-id="430af-125">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="430af-125">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430af-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="430af-126">-AsJob</span></span>
<span data-ttu-id="430af-127">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="430af-127">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="430af-128">-WhatIf</span></span>
<span data-ttu-id="430af-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="430af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="430af-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="430af-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="430af-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="430af-131">-Confirm</span></span>
<span data-ttu-id="430af-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="430af-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="430af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430af-133">CommonParameters</span></span>
<span data-ttu-id="430af-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="430af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430af-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="430af-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430af-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="430af-136">INPUTS</span></span>

## <span data-ttu-id="430af-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="430af-137">OUTPUTS</span></span>

### <span data-ttu-id="430af-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="430af-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="430af-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="430af-139">NOTES</span></span>

## <span data-ttu-id="430af-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="430af-140">RELATED LINKS</span></span>
