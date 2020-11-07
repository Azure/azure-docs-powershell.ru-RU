---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 8039da508110b47024be75967932719e5436f73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905869"
---
# <span data-ttu-id="2bbbf-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="2bbbf-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="2bbbf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2bbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbbf-103">Добавляет сервер v-Center, чтобы найти защищаемые элементы из.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="2bbbf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2bbbf-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bbbf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bbbf-105">DESCRIPTION</span></span>
<span data-ttu-id="2bbbf-106">Командлет **New-AzRecoveryServicesAsrvCenter** добавляет сервер vCenter, чтобы найти защищаемые элементы из.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="2bbbf-107">Этот командлет регистрирует vCenter Server для обнаружения с помощью сервера конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="2bbbf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2bbbf-108">EXAMPLES</span></span>

### <span data-ttu-id="2bbbf-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2bbbf-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="2bbbf-110">Добавляет сервер v-Center, чтобы найти защищаемые элементы из.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="2bbbf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2bbbf-111">PARAMETERS</span></span>

### <span data-ttu-id="2bbbf-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2bbbf-112">-Account</span></span>
<span data-ttu-id="2bbbf-113">Учетная запись пользователя для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-113">User login credential Account.</span></span>

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

### <span data-ttu-id="2bbbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bbbf-114">-DefaultProfile</span></span>
<span data-ttu-id="2bbbf-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bbbf-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="2bbbf-116">-Fabric</span></span>
<span data-ttu-id="2bbbf-117">Система ASR Fabric, соответствующая серверу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-117">ASR fabric corresponding to the Configuration server.</span></span>

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

### <span data-ttu-id="2bbbf-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="2bbbf-118">-IpOrHostName</span></span>
<span data-ttu-id="2bbbf-119">IPv4-адрес или полное доменное имя сервера vCenter.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="2bbbf-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2bbbf-120">-Name</span></span>
<span data-ttu-id="2bbbf-121">Понятное имя для сервера vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="2bbbf-122">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="2bbbf-122">-Port</span></span>
<span data-ttu-id="2bbbf-123">Порт TCP на сервере vCenter Server, который будет использоваться для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-123">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="2bbbf-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bbbf-124">-Confirm</span></span>
<span data-ttu-id="2bbbf-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bbbf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bbbf-126">-WhatIf</span></span>
<span data-ttu-id="2bbbf-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bbbf-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bbbf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbbf-129">CommonParameters</span></span>
<span data-ttu-id="2bbbf-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2bbbf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbbf-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bbbf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbbf-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2bbbf-132">INPUTS</span></span>

### <span data-ttu-id="2bbbf-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2bbbf-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2bbbf-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bbbf-134">OUTPUTS</span></span>

### <span data-ttu-id="2bbbf-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2bbbf-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2bbbf-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2bbbf-136">NOTES</span></span>

## <span data-ttu-id="2bbbf-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bbbf-137">RELATED LINKS</span></span>
