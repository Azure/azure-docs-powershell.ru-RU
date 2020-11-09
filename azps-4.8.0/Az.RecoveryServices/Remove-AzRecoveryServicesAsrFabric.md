---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244247"
---
# <span data-ttu-id="d7d6b-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d7d6b-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="d7d6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d6b-103">Удаляет указанную структуру восстановления сайта Azure из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="d7d6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7d6b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d6b-106">Командлет **Remove-AzRecoveryServicesAsrFabric** удаляет указанную структуру восстановления сайта Azure из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="d7d6b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-107">EXAMPLES</span></span>

### <span data-ttu-id="d7d6b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7d6b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="d7d6b-109">Запускает удаление указанной структуры и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d7d6b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-110">PARAMETERS</span></span>

### <span data-ttu-id="d7d6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d6b-111">-DefaultProfile</span></span>
<span data-ttu-id="d7d6b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d7d6b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d7d6b-113">-Force</span></span>
<span data-ttu-id="d7d6b-114">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="d7d6b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7d6b-115">-InputObject</span></span>
<span data-ttu-id="d7d6b-116">Входной объект для командлета: объект Fabric ASR, соответствующий удаляемой структуре.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="d7d6b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7d6b-117">-Confirm</span></span>
<span data-ttu-id="d7d6b-118">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-118">Specify if confirmation is required.</span></span> <span data-ttu-id="d7d6b-119">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="d7d6b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d6b-120">-WhatIf</span></span>
<span data-ttu-id="d7d6b-121">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="d7d6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d6b-122">CommonParameters</span></span>
<span data-ttu-id="d7d6b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d6b-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7d6b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d6b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7d6b-125">INPUTS</span></span>

### <span data-ttu-id="d7d6b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d7d6b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d7d6b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-127">OUTPUTS</span></span>

### <span data-ttu-id="d7d6b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d7d6b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d7d6b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7d6b-129">NOTES</span></span>

## <span data-ttu-id="d7d6b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-130">RELATED LINKS</span></span>

[<span data-ttu-id="d7d6b-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d7d6b-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="d7d6b-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d7d6b-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)