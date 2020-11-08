---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246841"
---
# <span data-ttu-id="a77b9-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a77b9-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="a77b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a77b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a77b9-103">Обновляет указанное сетевое сопоставление для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="a77b9-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="a77b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a77b9-104">SYNTAX</span></span>

### <span data-ttu-id="a77b9-105">ByNetworkObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a77b9-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a77b9-106">ById</span><span class="sxs-lookup"><span data-stu-id="a77b9-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a77b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a77b9-107">DESCRIPTION</span></span>
<span data-ttu-id="a77b9-108">Командлет **Update-AzRecoveryServicesAsrNetworkMapping** обновляет указанное сетевое сопоставление для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="a77b9-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="a77b9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a77b9-109">EXAMPLES</span></span>

### <span data-ttu-id="a77b9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a77b9-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="a77b9-111">Запускает операцию обновления сетевого сопоставления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="a77b9-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a77b9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a77b9-112">PARAMETERS</span></span>

### <span data-ttu-id="a77b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a77b9-113">-DefaultProfile</span></span>
<span data-ttu-id="a77b9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a77b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a77b9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a77b9-115">-InputObject</span></span>
<span data-ttu-id="a77b9-116">Объект input: определяет объект сетевого сопоставления ASR, соответствующий сетевому сопоставлению ASR для обновления.</span><span class="sxs-lookup"><span data-stu-id="a77b9-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a77b9-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="a77b9-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="a77b9-118">Указывает идентификатор сети Azure Recovery Network для сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a77b9-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77b9-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="a77b9-119">-RecoveryNetwork</span></span>
<span data-ttu-id="a77b9-120">Указывает сетевой объект для восстановления сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a77b9-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77b9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a77b9-121">-Confirm</span></span>
<span data-ttu-id="a77b9-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a77b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a77b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a77b9-123">-WhatIf</span></span>
<span data-ttu-id="a77b9-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a77b9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a77b9-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a77b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a77b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77b9-126">CommonParameters</span></span>
<span data-ttu-id="a77b9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a77b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77b9-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a77b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77b9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a77b9-129">INPUTS</span></span>

### <span data-ttu-id="a77b9-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a77b9-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="a77b9-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a77b9-131">OUTPUTS</span></span>

### <span data-ttu-id="a77b9-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a77b9-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a77b9-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a77b9-133">NOTES</span></span>

## <span data-ttu-id="a77b9-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a77b9-134">RELATED LINKS</span></span>
