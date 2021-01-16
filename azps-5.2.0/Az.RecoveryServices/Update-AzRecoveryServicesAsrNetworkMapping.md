---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394172"
---
# <span data-ttu-id="6361c-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6361c-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="6361c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6361c-102">SYNOPSIS</span></span>
<span data-ttu-id="6361c-103">Обновляет указанное сопоставление сети восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="6361c-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="6361c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6361c-104">SYNTAX</span></span>

### <span data-ttu-id="6361c-105">ByNetworkObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6361c-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6361c-106">ById</span><span class="sxs-lookup"><span data-stu-id="6361c-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6361c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6361c-107">DESCRIPTION</span></span>
<span data-ttu-id="6361c-108">Командлет **Update-AzRecoveryServicesAsrNetworkMapping** обновляет указанное сопоставление сети восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="6361c-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="6361c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6361c-109">EXAMPLES</span></span>

### <span data-ttu-id="6361c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6361c-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="6361c-111">Запускает операцию обновления сетевого сопоставления с использованием указанных параметров и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="6361c-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6361c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6361c-112">PARAMETERS</span></span>

### <span data-ttu-id="6361c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6361c-113">-DefaultProfile</span></span>
<span data-ttu-id="6361c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6361c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6361c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6361c-115">-InputObject</span></span>
<span data-ttu-id="6361c-116">Объект ввода: определяет объект сетевого сопоставления ASR, соответствующий обновляемой сопоставлению сети ASR.</span><span class="sxs-lookup"><span data-stu-id="6361c-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="6361c-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6361c-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="6361c-118">Определяет для сопоставления сетей ИД сети Azure для восстановления.</span><span class="sxs-lookup"><span data-stu-id="6361c-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="6361c-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="6361c-119">-RecoveryNetwork</span></span>
<span data-ttu-id="6361c-120">Определяет объект сети восстановления для сопоставления сетей.</span><span class="sxs-lookup"><span data-stu-id="6361c-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="6361c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6361c-121">-Confirm</span></span>
<span data-ttu-id="6361c-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6361c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6361c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6361c-123">-WhatIf</span></span>
<span data-ttu-id="6361c-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6361c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6361c-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6361c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6361c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6361c-126">CommonParameters</span></span>
<span data-ttu-id="6361c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6361c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6361c-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6361c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6361c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6361c-129">INPUTS</span></span>

### <span data-ttu-id="6361c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6361c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="6361c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6361c-131">OUTPUTS</span></span>

### <span data-ttu-id="6361c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6361c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6361c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6361c-133">NOTES</span></span>

## <span data-ttu-id="6361c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6361c-134">RELATED LINKS</span></span>
