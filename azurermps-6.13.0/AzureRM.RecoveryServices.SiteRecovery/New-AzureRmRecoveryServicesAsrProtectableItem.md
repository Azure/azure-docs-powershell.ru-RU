---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c5d86909bffa7c38d66c31b56b34a66251b21d65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556547"
---
# <span data-ttu-id="ed16b-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ed16b-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="ed16b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed16b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed16b-103">Добавьте (разобнаружение) физический сервер в список защищенных элементов.</span><span class="sxs-lookup"><span data-stu-id="ed16b-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed16b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed16b-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed16b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed16b-105">DESCRIPTION</span></span>
<span data-ttu-id="ed16b-106">**New-AzureRmRecoveryServicesAsrProtectableItem** добавляет новый защищенный элемент в список обнаруженных защищаемых элементов в контейнере защиты в структуре ASR (применимо только к типу фабрики VMware).</span><span class="sxs-lookup"><span data-stu-id="ed16b-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="ed16b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed16b-107">EXAMPLES</span></span>

### <span data-ttu-id="ed16b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed16b-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="ed16b-109">Добавьте ProtectableItem и найдите новую службу восстановления Azure.</span><span class="sxs-lookup"><span data-stu-id="ed16b-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="ed16b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed16b-110">PARAMETERS</span></span>

### <span data-ttu-id="ed16b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed16b-111">-DefaultProfile</span></span>
<span data-ttu-id="ed16b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed16b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed16b-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ed16b-113">-FriendlyName</span></span>
<span data-ttu-id="ed16b-114">Понятное имя для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="ed16b-114">Friendly name for the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed16b-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="ed16b-115">-IPAddress</span></span>
<span data-ttu-id="ed16b-116">IP-адрес защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="ed16b-116">IP address of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed16b-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="ed16b-117">-OSType</span></span>
<span data-ttu-id="ed16b-118">Тип операционной системы (Windows или Linux) защищаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="ed16b-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed16b-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ed16b-119">-ProtectionContainer</span></span>
<span data-ttu-id="ed16b-120">Объект контейнера защиты ASR, в который нужно добавить защищенный элемент.</span><span class="sxs-lookup"><span data-stu-id="ed16b-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed16b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed16b-121">-Confirm</span></span>
<span data-ttu-id="ed16b-122">Запрашивать подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed16b-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed16b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed16b-123">-WhatIf</span></span>
<span data-ttu-id="ed16b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed16b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed16b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed16b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed16b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed16b-126">CommonParameters</span></span>
<span data-ttu-id="ed16b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed16b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed16b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed16b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed16b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed16b-129">INPUTS</span></span>

### <span data-ttu-id="ed16b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ed16b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="ed16b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed16b-131">OUTPUTS</span></span>

### <span data-ttu-id="ed16b-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed16b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed16b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed16b-133">NOTES</span></span>

## <span data-ttu-id="ed16b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed16b-134">RELATED LINKS</span></span>
