---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: c27d4d88dd4c2fdf86db5ca39d608add2feb845f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556539"
---
# <span data-ttu-id="8d12d-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="8d12d-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="8d12d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d12d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d12d-103">Добавляет сервер v-Center, чтобы найти защищаемые элементы из.</span><span class="sxs-lookup"><span data-stu-id="8d12d-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d12d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d12d-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d12d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d12d-105">DESCRIPTION</span></span>
<span data-ttu-id="8d12d-106">Командлет **New-AzureRmRecoveryServicesAsrvCenter** добавляет сервер vCenter, чтобы найти защищаемые элементы из.</span><span class="sxs-lookup"><span data-stu-id="8d12d-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="8d12d-107">Этот командлет регистрирует vCenter Server для обнаружения с помощью сервера конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8d12d-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="8d12d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d12d-108">EXAMPLES</span></span>

### <span data-ttu-id="8d12d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d12d-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="8d12d-110">Добавляет сервер v-Center, чтобы найти защищаемые элементы из.</span><span class="sxs-lookup"><span data-stu-id="8d12d-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="8d12d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d12d-111">PARAMETERS</span></span>

### <span data-ttu-id="8d12d-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8d12d-112">-Account</span></span>
<span data-ttu-id="8d12d-113">Учетная запись пользователя для входа в creadential.</span><span class="sxs-lookup"><span data-stu-id="8d12d-113">User login creadential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d12d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d12d-114">-DefaultProfile</span></span>
<span data-ttu-id="8d12d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d12d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d12d-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="8d12d-116">-Fabric</span></span>
<span data-ttu-id="8d12d-117">Система ASR Fabric, соответствующая серверу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8d12d-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d12d-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="8d12d-118">-IpOrHostName</span></span>
<span data-ttu-id="8d12d-119">IPv4-адрес или полное доменное имя сервера vCenter.</span><span class="sxs-lookup"><span data-stu-id="8d12d-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="8d12d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d12d-120">-Name</span></span>
<span data-ttu-id="8d12d-121">Понятное имя для сервера vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="8d12d-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="8d12d-122">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="8d12d-122">-Port</span></span>
<span data-ttu-id="8d12d-123">Порт TCP на сервере vCenter Server, который будет использоваться для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="8d12d-123">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="8d12d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d12d-124">-Confirm</span></span>
<span data-ttu-id="8d12d-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d12d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d12d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d12d-126">-WhatIf</span></span>
<span data-ttu-id="8d12d-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d12d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d12d-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d12d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d12d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d12d-129">CommonParameters</span></span>
<span data-ttu-id="8d12d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d12d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d12d-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d12d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d12d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d12d-132">INPUTS</span></span>

### <span data-ttu-id="8d12d-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8d12d-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8d12d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d12d-134">OUTPUTS</span></span>

### <span data-ttu-id="8d12d-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="8d12d-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8d12d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d12d-136">NOTES</span></span>

## <span data-ttu-id="8d12d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d12d-137">RELATED LINKS</span></span>
