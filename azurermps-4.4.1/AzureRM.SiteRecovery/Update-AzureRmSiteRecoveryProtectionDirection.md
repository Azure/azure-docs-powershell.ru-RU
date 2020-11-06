---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562060"
---
# <span data-ttu-id="7af9c-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="7af9c-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="7af9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7af9c-102">SYNOPSIS</span></span>
<span data-ttu-id="7af9c-103">Обновляет исходный и целевой сервер для защиты объекта восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="7af9c-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7af9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7af9c-104">SYNTAX</span></span>

### <span data-ttu-id="7af9c-105">ByPEObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7af9c-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7af9c-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7af9c-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7af9c-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="7af9c-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7af9c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7af9c-108">DESCRIPTION</span></span>
<span data-ttu-id="7af9c-109">Командлет **Update-AzureRmSiteRecoveryProtectionDirection** обновляет исходный и целевой сервер для защиты объекта Azure Site Recovery по завершении операции фиксации отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="7af9c-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="7af9c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7af9c-110">EXAMPLES</span></span>

## <span data-ttu-id="7af9c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7af9c-111">PARAMETERS</span></span>

### <span data-ttu-id="7af9c-112">-Направление</span><span class="sxs-lookup"><span data-stu-id="7af9c-112">-Direction</span></span>
<span data-ttu-id="7af9c-113">Указывает направление фиксации.</span><span class="sxs-lookup"><span data-stu-id="7af9c-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="7af9c-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7af9c-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7af9c-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="7af9c-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="7af9c-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="7af9c-116">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af9c-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7af9c-117">-ProtectionEntity</span></span>
<span data-ttu-id="7af9c-118">Указывает объект сущности для защиты.</span><span class="sxs-lookup"><span data-stu-id="7af9c-118">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7af9c-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7af9c-119">-RecoveryPlan</span></span>
<span data-ttu-id="7af9c-120">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="7af9c-120">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7af9c-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7af9c-121">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7af9c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af9c-122">-DefaultProfile</span></span>
<span data-ttu-id="7af9c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7af9c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7af9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af9c-124">CommonParameters</span></span>
<span data-ttu-id="7af9c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7af9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af9c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7af9c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af9c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7af9c-127">INPUTS</span></span>

### <span data-ttu-id="7af9c-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7af9c-128">ASRProtectionEntity</span></span>
<span data-ttu-id="7af9c-129">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7af9c-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="7af9c-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7af9c-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="7af9c-131">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7af9c-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="7af9c-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7af9c-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="7af9c-133">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7af9c-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="7af9c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7af9c-134">OUTPUTS</span></span>

### <span data-ttu-id="7af9c-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7af9c-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7af9c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7af9c-136">NOTES</span></span>

## <span data-ttu-id="7af9c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7af9c-137">RELATED LINKS</span></span>

