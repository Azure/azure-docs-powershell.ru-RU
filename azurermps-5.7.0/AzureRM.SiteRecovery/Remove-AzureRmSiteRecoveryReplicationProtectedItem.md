---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 121d45d626a226542f495cd197781b795823b1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567883"
---
# <span data-ttu-id="18f1d-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="18f1d-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="18f1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="18f1d-103">Удаляет защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="18f1d-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18f1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18f1d-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18f1d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="18f1d-106">Командлет **Remove-AzureRmSiteRecoveryReplicationProtectedItem** удаляет защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="18f1d-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="18f1d-107">Эта операция приводит к остановке репликации для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="18f1d-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="18f1d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18f1d-108">EXAMPLES</span></span>

## <span data-ttu-id="18f1d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18f1d-109">PARAMETERS</span></span>

### <span data-ttu-id="18f1d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f1d-110">-DefaultProfile</span></span>
<span data-ttu-id="18f1d-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18f1d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f1d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="18f1d-112">-Force</span></span>
<span data-ttu-id="18f1d-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="18f1d-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f1d-114">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="18f1d-114">-ReplicationProtectedItem</span></span>
<span data-ttu-id="18f1d-115">Указывает объект защищенного элемента репликации.</span><span class="sxs-lookup"><span data-stu-id="18f1d-115">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18f1d-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="18f1d-116">-WaitForCompletion</span></span>
<span data-ttu-id="18f1d-117">Указывает на то, что командлет ожидает завершения операции.</span><span class="sxs-lookup"><span data-stu-id="18f1d-117">Indicates that the cmdlet waits for the operation to complete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f1d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18f1d-118">-Confirm</span></span>
<span data-ttu-id="18f1d-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="18f1d-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f1d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18f1d-120">-WhatIf</span></span>
<span data-ttu-id="18f1d-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="18f1d-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="18f1d-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="18f1d-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f1d-123">CommonParameters</span></span>
<span data-ttu-id="18f1d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18f1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f1d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f1d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f1d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18f1d-126">INPUTS</span></span>

### <span data-ttu-id="18f1d-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="18f1d-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="18f1d-128">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="18f1d-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="18f1d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18f1d-129">OUTPUTS</span></span>

### <span data-ttu-id="18f1d-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="18f1d-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="18f1d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="18f1d-131">NOTES</span></span>

## <span data-ttu-id="18f1d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18f1d-132">RELATED LINKS</span></span>

[<span data-ttu-id="18f1d-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="18f1d-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="18f1d-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="18f1d-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="18f1d-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="18f1d-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
