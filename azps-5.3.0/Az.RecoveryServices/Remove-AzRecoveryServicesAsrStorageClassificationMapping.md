---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506795"
---
# <span data-ttu-id="bcde9-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bcde9-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="bcde9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcde9-102">SYNOPSIS</span></span>
<span data-ttu-id="bcde9-103">Удаляет указанное сопоставление классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="bcde9-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="bcde9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcde9-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcde9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcde9-105">DESCRIPTION</span></span>
<span data-ttu-id="bcde9-106">С **его использованием** удаляется указанное сопоставление классификации хранилища для восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="bcde9-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="bcde9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcde9-107">EXAMPLES</span></span>

### <span data-ttu-id="bcde9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bcde9-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="bcde9-109">Начало удаления указанного сопоставления классификации хранилища и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="bcde9-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bcde9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcde9-110">PARAMETERS</span></span>

### <span data-ttu-id="bcde9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcde9-111">-DefaultProfile</span></span>
<span data-ttu-id="bcde9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcde9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bcde9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcde9-113">-InputObject</span></span>
<span data-ttu-id="bcde9-114">Объект ввода для cmdlet: объект сопоставления классификации хранилища ASR, соответствующий удаляемой классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="bcde9-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="bcde9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcde9-115">-Confirm</span></span>
<span data-ttu-id="bcde9-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bcde9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcde9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcde9-117">-WhatIf</span></span>
<span data-ttu-id="bcde9-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcde9-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcde9-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bcde9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcde9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcde9-120">CommonParameters</span></span>
<span data-ttu-id="bcde9-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcde9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcde9-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcde9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcde9-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcde9-123">INPUTS</span></span>

### <span data-ttu-id="bcde9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bcde9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="bcde9-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcde9-125">OUTPUTS</span></span>

### <span data-ttu-id="bcde9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="bcde9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bcde9-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcde9-127">NOTES</span></span>

## <span data-ttu-id="bcde9-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcde9-128">RELATED LINKS</span></span>

[<span data-ttu-id="bcde9-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bcde9-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="bcde9-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bcde9-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
