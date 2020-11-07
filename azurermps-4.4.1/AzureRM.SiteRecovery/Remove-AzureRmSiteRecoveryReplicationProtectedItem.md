---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734215"
---
# <span data-ttu-id="88eb4-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="88eb4-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="88eb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="88eb4-103">Удаляет защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="88eb4-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88eb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88eb4-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88eb4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="88eb4-106">Командлет **Remove-AzureRmSiteRecoveryReplicationProtectedItem** удаляет защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="88eb4-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="88eb4-107">Эта операция приводит к остановке репликации для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="88eb4-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="88eb4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88eb4-108">EXAMPLES</span></span>

## <span data-ttu-id="88eb4-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88eb4-109">PARAMETERS</span></span>

### <span data-ttu-id="88eb4-110">-Force</span><span class="sxs-lookup"><span data-stu-id="88eb4-110">-Force</span></span>
<span data-ttu-id="88eb4-111">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="88eb4-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88eb4-112">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="88eb4-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="88eb4-113">Указывает объект защищенного элемента репликации.</span><span class="sxs-lookup"><span data-stu-id="88eb4-113">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88eb4-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="88eb4-114">-WaitForCompletion</span></span>
<span data-ttu-id="88eb4-115">Указывает на то, что командлет ожидает завершения операции.</span><span class="sxs-lookup"><span data-stu-id="88eb4-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="88eb4-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88eb4-116">-Confirm</span></span>
<span data-ttu-id="88eb4-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88eb4-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88eb4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88eb4-118">-WhatIf</span></span>
<span data-ttu-id="88eb4-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88eb4-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="88eb4-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88eb4-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88eb4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88eb4-121">-DefaultProfile</span></span>
<span data-ttu-id="88eb4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88eb4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88eb4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88eb4-123">CommonParameters</span></span>
<span data-ttu-id="88eb4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88eb4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88eb4-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88eb4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88eb4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88eb4-126">INPUTS</span></span>

### <span data-ttu-id="88eb4-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="88eb4-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="88eb4-128">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="88eb4-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="88eb4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88eb4-129">OUTPUTS</span></span>

### <span data-ttu-id="88eb4-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="88eb4-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="88eb4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="88eb4-131">NOTES</span></span>

## <span data-ttu-id="88eb4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88eb4-132">RELATED LINKS</span></span>

[<span data-ttu-id="88eb4-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="88eb4-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="88eb4-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="88eb4-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="88eb4-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="88eb4-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
