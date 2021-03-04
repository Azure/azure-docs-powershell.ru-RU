---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8ad9ca87687acfdeb526dc33cdcb5a6ec70c65bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953416"
---
# <span data-ttu-id="64a61-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="64a61-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="64a61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64a61-102">SYNOPSIS</span></span>
<span data-ttu-id="64a61-103">Создает сопоставление классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="64a61-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="64a61-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64a61-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a61-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64a61-105">DESCRIPTION</span></span>
<span data-ttu-id="64a61-106">Для создания классификации хранилища, сопоставленной со службами восстановления, создается **cmdlet New-AzRecoveryServicesAsrStorageClassificationMapping.**</span><span class="sxs-lookup"><span data-stu-id="64a61-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="64a61-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64a61-107">EXAMPLES</span></span>

### <span data-ttu-id="64a61-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64a61-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="64a61-109">Начало операции создания сопоставления классификации хранилища с указанными параметрами и возврат задания asR, используемого для ее отслеживания.</span><span class="sxs-lookup"><span data-stu-id="64a61-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="64a61-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64a61-110">PARAMETERS</span></span>

### <span data-ttu-id="64a61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a61-111">-DefaultProfile</span></span>
<span data-ttu-id="64a61-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64a61-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="64a61-113">-Name</span><span class="sxs-lookup"><span data-stu-id="64a61-113">-Name</span></span>
<span data-ttu-id="64a61-114">Указывает имя для сопоставления классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="64a61-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="64a61-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="64a61-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="64a61-116">Указывает основной объект классификации хранилища ASR для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="64a61-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64a61-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="64a61-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="64a61-118">Определяет объект классификации хранилища для восстановления для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="64a61-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a61-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64a61-119">-Confirm</span></span>
<span data-ttu-id="64a61-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="64a61-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a61-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a61-121">-WhatIf</span></span>
<span data-ttu-id="64a61-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a61-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64a61-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="64a61-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a61-124">CommonParameters</span></span>
<span data-ttu-id="64a61-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a61-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64a61-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a61-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64a61-127">INPUTS</span></span>

### <span data-ttu-id="64a61-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="64a61-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="64a61-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64a61-129">OUTPUTS</span></span>

### <span data-ttu-id="64a61-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="64a61-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64a61-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64a61-131">NOTES</span></span>

## <span data-ttu-id="64a61-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64a61-132">RELATED LINKS</span></span>

[<span data-ttu-id="64a61-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="64a61-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="64a61-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="64a61-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
