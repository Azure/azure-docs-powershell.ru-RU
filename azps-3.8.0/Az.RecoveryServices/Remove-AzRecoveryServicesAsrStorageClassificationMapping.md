---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072624"
---
# <span data-ttu-id="afb21-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="afb21-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="afb21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="afb21-102">SYNOPSIS</span></span>
<span data-ttu-id="afb21-103">Удаляет указанное сопоставление классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="afb21-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="afb21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="afb21-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afb21-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb21-105">DESCRIPTION</span></span>
<span data-ttu-id="afb21-106">Командлет **Remove-AzRecoveryServicesAsrStorageClassificationMapping** удаляет указанное сопоставление классификации хранилища для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="afb21-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="afb21-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="afb21-107">EXAMPLES</span></span>

### <span data-ttu-id="afb21-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="afb21-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="afb21-109">Запускает удаление указанного сопоставления классификации хранилища и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="afb21-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="afb21-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="afb21-110">PARAMETERS</span></span>

### <span data-ttu-id="afb21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb21-111">-DefaultProfile</span></span>
<span data-ttu-id="afb21-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afb21-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="afb21-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afb21-113">-InputObject</span></span>
<span data-ttu-id="afb21-114">Входной объект для командлета: объект сопоставления классификации хранилища ASR, соответствующий сопоставлению классификации хранилища ASR, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="afb21-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afb21-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afb21-115">-Confirm</span></span>
<span data-ttu-id="afb21-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="afb21-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb21-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb21-117">-WhatIf</span></span>
<span data-ttu-id="afb21-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="afb21-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afb21-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="afb21-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb21-120">CommonParameters</span></span>
<span data-ttu-id="afb21-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="afb21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb21-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afb21-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb21-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="afb21-123">INPUTS</span></span>

### <span data-ttu-id="afb21-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="afb21-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="afb21-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb21-125">OUTPUTS</span></span>

### <span data-ttu-id="afb21-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="afb21-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="afb21-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="afb21-127">NOTES</span></span>

## <span data-ttu-id="afb21-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afb21-128">RELATED LINKS</span></span>

[<span data-ttu-id="afb21-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="afb21-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="afb21-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="afb21-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
