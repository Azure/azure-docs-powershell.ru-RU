---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516870"
---
# <span data-ttu-id="35dca-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="35dca-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="35dca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35dca-102">SYNOPSIS</span></span>
<span data-ttu-id="35dca-103">Удаление и удаление указанного поставщика служб восстановления сайтов Azure из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="35dca-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="35dca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35dca-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35dca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35dca-105">DESCRIPTION</span></span>
<span data-ttu-id="35dca-106">Из хранилища удаляется указанный поставщик служб восстановления сайтов Azure— **AzRecoveryServicesAsrServicesProvider.**</span><span class="sxs-lookup"><span data-stu-id="35dca-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="35dca-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35dca-107">EXAMPLES</span></span>

### <span data-ttu-id="35dca-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35dca-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="35dca-109">Запускает удаление или удаление указанного поставщика служб восстановления сайтов Azure и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="35dca-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="35dca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35dca-110">PARAMETERS</span></span>

### <span data-ttu-id="35dca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35dca-111">-DefaultProfile</span></span>
<span data-ttu-id="35dca-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35dca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="35dca-113">-Force</span><span class="sxs-lookup"><span data-stu-id="35dca-113">-Force</span></span>
<span data-ttu-id="35dca-114">Принудительно выполнить команду, не предоставляя дополнительное предупреждение.</span><span class="sxs-lookup"><span data-stu-id="35dca-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="35dca-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35dca-115">-InputObject</span></span>
<span data-ttu-id="35dca-116">Объект ввода для cmdlet: объект поставщика услуг восстановления ASR, соответствующий поставщику услуг восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="35dca-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35dca-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35dca-117">-Confirm</span></span>
<span data-ttu-id="35dca-118">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="35dca-118">Specify if confirmation is required.</span></span> <span data-ttu-id="35dca-119">Заданное значение параметра подтверждения будет $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="35dca-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="35dca-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35dca-120">-WhatIf</span></span>
<span data-ttu-id="35dca-121">Показывает, что произойдет, если выполняется cmdlet без его выполнения.</span><span class="sxs-lookup"><span data-stu-id="35dca-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="35dca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dca-122">CommonParameters</span></span>
<span data-ttu-id="35dca-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dca-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35dca-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dca-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35dca-125">INPUTS</span></span>

### <span data-ttu-id="35dca-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="35dca-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="35dca-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35dca-127">OUTPUTS</span></span>

### <span data-ttu-id="35dca-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="35dca-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="35dca-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35dca-129">NOTES</span></span>

## <span data-ttu-id="35dca-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35dca-130">RELATED LINKS</span></span>

[<span data-ttu-id="35dca-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="35dca-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="35dca-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="35dca-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
