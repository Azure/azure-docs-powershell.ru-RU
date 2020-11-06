---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557264"
---
# <span data-ttu-id="0a071-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="0a071-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="0a071-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a071-102">SYNOPSIS</span></span>
<span data-ttu-id="0a071-103">Создает объект сопоставления дисков для реплицируемых дисков виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="0a071-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a071-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a071-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a071-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a071-105">DESCRIPTION</span></span>
<span data-ttu-id="0a071-106">Создает объект сопоставления дисков, который сопоставляет диск виртуальной машины Azure с учетной записью хранения кэша и целевой учетной записью хранилища (областью восстановления), которая будет использоваться для репликации диска.</span><span class="sxs-lookup"><span data-stu-id="0a071-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="0a071-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a071-107">EXAMPLES</span></span>

### <span data-ttu-id="0a071-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a071-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="0a071-109">Создайте объект сопоставления дисков для дисков виртуальных машин Azure, которые нужно реплицировать. Используется во время работы Azure для Azure и повторной защиты.</span><span class="sxs-lookup"><span data-stu-id="0a071-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="0a071-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a071-110">PARAMETERS</span></span>

### <span data-ttu-id="0a071-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a071-111">-Confirm</span></span>
<span data-ttu-id="0a071-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a071-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a071-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a071-113">-DefaultProfile</span></span>
<span data-ttu-id="0a071-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a071-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a071-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0a071-115">-LogStorageAccountId</span></span>
<span data-ttu-id="0a071-116">Указывает идентификатор журнала или учетной записи для хранения кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="0a071-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a071-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0a071-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="0a071-118">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="0a071-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a071-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="0a071-119">-VhdUri</span></span>
<span data-ttu-id="0a071-120">Укажите URI виртуального жесткого диска, которому соответствует это сопоставление.</span><span class="sxs-lookup"><span data-stu-id="0a071-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a071-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a071-121">-WhatIf</span></span>
<span data-ttu-id="0a071-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a071-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a071-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a071-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a071-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a071-124">CommonParameters</span></span>
<span data-ttu-id="0a071-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a071-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a071-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a071-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a071-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a071-127">INPUTS</span></span>

### <span data-ttu-id="0a071-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="0a071-128">None</span></span>

## <span data-ttu-id="0a071-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a071-129">OUTPUTS</span></span>

### <span data-ttu-id="0a071-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="0a071-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="0a071-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a071-131">NOTES</span></span>

## <span data-ttu-id="0a071-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a071-132">RELATED LINKS</span></span>
