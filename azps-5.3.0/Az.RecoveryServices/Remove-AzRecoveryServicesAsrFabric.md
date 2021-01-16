---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506746"
---
# <span data-ttu-id="4ef89-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4ef89-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="4ef89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef89-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef89-103">Удаляет указанную ткань восстановления сайта Azure из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4ef89-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="4ef89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ef89-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ef89-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ef89-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef89-106">Для удаления указанной структуры восстановления сайтов Azure из хранилища служб восстановления удаляется указанный материал Azure **AzRecoveryServicesAsrFabric.**</span><span class="sxs-lookup"><span data-stu-id="4ef89-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="4ef89-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ef89-107">EXAMPLES</span></span>

### <span data-ttu-id="4ef89-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ef89-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="4ef89-109">Начало удаления указанной тканью и возврат задания asR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="4ef89-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4ef89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ef89-110">PARAMETERS</span></span>

### <span data-ttu-id="4ef89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef89-111">-DefaultProfile</span></span>
<span data-ttu-id="4ef89-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ef89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4ef89-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4ef89-113">-Force</span></span>
<span data-ttu-id="4ef89-114">Принудительно выполнить команду, не предоставляя дополнительное предупреждение.</span><span class="sxs-lookup"><span data-stu-id="4ef89-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="4ef89-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ef89-115">-InputObject</span></span>
<span data-ttu-id="4ef89-116">Объект ввода для cmdlet: объект asR-ткань, соответствующий удаляемой тканью.</span><span class="sxs-lookup"><span data-stu-id="4ef89-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef89-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ef89-117">-Confirm</span></span>
<span data-ttu-id="4ef89-118">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4ef89-118">Specify if confirmation is required.</span></span> <span data-ttu-id="4ef89-119">Заданное значение параметра подтверждения будет $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4ef89-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="4ef89-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef89-120">-WhatIf</span></span>
<span data-ttu-id="4ef89-121">Показывает, что произойдет, если выполняется cmdlet без его выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ef89-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="4ef89-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef89-122">CommonParameters</span></span>
<span data-ttu-id="4ef89-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef89-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef89-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ef89-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef89-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ef89-125">INPUTS</span></span>

### <span data-ttu-id="4ef89-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4ef89-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4ef89-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ef89-127">OUTPUTS</span></span>

### <span data-ttu-id="4ef89-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4ef89-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4ef89-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ef89-129">NOTES</span></span>

## <span data-ttu-id="4ef89-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ef89-130">RELATED LINKS</span></span>

[<span data-ttu-id="4ef89-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4ef89-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="4ef89-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4ef89-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
