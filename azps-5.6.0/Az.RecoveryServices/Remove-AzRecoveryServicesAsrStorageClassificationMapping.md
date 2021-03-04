---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: b19808ff7b5576c93bc81414d665e23086e524d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953139"
---
# <span data-ttu-id="004fc-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="004fc-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="004fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="004fc-102">SYNOPSIS</span></span>
<span data-ttu-id="004fc-103">Удаляет указанное сопоставление классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="004fc-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="004fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="004fc-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="004fc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="004fc-105">DESCRIPTION</span></span>
<span data-ttu-id="004fc-106">Для удаления указанного сопоставления классификации хранилища для восстановления сайтов Azure удаляется cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping.**</span><span class="sxs-lookup"><span data-stu-id="004fc-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="004fc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="004fc-107">EXAMPLES</span></span>

### <span data-ttu-id="004fc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="004fc-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="004fc-109">Начало удаления указанного сопоставления классификации хранилища и возврат задания asR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="004fc-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="004fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="004fc-110">PARAMETERS</span></span>

### <span data-ttu-id="004fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004fc-111">-DefaultProfile</span></span>
<span data-ttu-id="004fc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="004fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="004fc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="004fc-113">-InputObject</span></span>
<span data-ttu-id="004fc-114">Объект ввода для cmdlet: объект сопоставления классификации хранилища ASR, соответствующий удаляемой классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="004fc-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="004fc-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="004fc-115">-Confirm</span></span>
<span data-ttu-id="004fc-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="004fc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="004fc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004fc-117">-WhatIf</span></span>
<span data-ttu-id="004fc-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="004fc-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="004fc-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="004fc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="004fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004fc-120">CommonParameters</span></span>
<span data-ttu-id="004fc-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004fc-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="004fc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004fc-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="004fc-123">INPUTS</span></span>

### <span data-ttu-id="004fc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="004fc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="004fc-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="004fc-125">OUTPUTS</span></span>

### <span data-ttu-id="004fc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="004fc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="004fc-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="004fc-127">NOTES</span></span>

## <span data-ttu-id="004fc-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="004fc-128">RELATED LINKS</span></span>

[<span data-ttu-id="004fc-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="004fc-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="004fc-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="004fc-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
