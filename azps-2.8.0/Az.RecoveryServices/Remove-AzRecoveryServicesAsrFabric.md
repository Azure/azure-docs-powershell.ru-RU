---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905862"
---
# <span data-ttu-id="5efc4-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5efc4-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="5efc4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5efc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5efc4-103">Удаляет указанную структуру восстановления сайта Azure из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5efc4-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="5efc4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5efc4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5efc4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5efc4-105">DESCRIPTION</span></span>
<span data-ttu-id="5efc4-106">Командлет **Remove-AzRecoveryServicesAsrFabric** удаляет указанную структуру восстановления сайта Azure из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5efc4-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="5efc4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5efc4-107">EXAMPLES</span></span>

### <span data-ttu-id="5efc4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5efc4-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="5efc4-109">Запускает удаление указанной структуры и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="5efc4-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5efc4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5efc4-110">PARAMETERS</span></span>

### <span data-ttu-id="5efc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5efc4-111">-DefaultProfile</span></span>
<span data-ttu-id="5efc4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5efc4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5efc4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5efc4-113">-Force</span></span>
<span data-ttu-id="5efc4-114">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="5efc4-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="5efc4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5efc4-115">-InputObject</span></span>
<span data-ttu-id="5efc4-116">Входной объект для командлета: объект Fabric ASR, соответствующий удаляемой структуре.</span><span class="sxs-lookup"><span data-stu-id="5efc4-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="5efc4-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5efc4-117">-Confirm</span></span>
<span data-ttu-id="5efc4-118">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5efc4-118">Specify if confirmation is required.</span></span> <span data-ttu-id="5efc4-119">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5efc4-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="5efc4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5efc4-120">-WhatIf</span></span>
<span data-ttu-id="5efc4-121">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="5efc4-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="5efc4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5efc4-122">CommonParameters</span></span>
<span data-ttu-id="5efc4-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5efc4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5efc4-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5efc4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5efc4-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5efc4-125">INPUTS</span></span>

### <span data-ttu-id="5efc4-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5efc4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5efc4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5efc4-127">OUTPUTS</span></span>

### <span data-ttu-id="5efc4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5efc4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5efc4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5efc4-129">NOTES</span></span>

## <span data-ttu-id="5efc4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5efc4-130">RELATED LINKS</span></span>

[<span data-ttu-id="5efc4-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5efc4-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="5efc4-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5efc4-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
