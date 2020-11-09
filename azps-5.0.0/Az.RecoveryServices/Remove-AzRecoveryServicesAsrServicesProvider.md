---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248031"
---
# <span data-ttu-id="e6ea4-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e6ea4-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="e6ea4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ea4-103">Удаление и Отмена регистрации указанного поставщика служб восстановления Azure Site Recovery из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="e6ea4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6ea4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ea4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ea4-106">Командлет **Remove-AzRecoveryServicesAsrServicesProvider** удаляет из хранилища указанный поставщик служб восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="e6ea4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6ea4-107">EXAMPLES</span></span>

### <span data-ttu-id="e6ea4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6ea4-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="e6ea4-109">Запускает удаление и отмену регистрации указанного поставщика служб Azure Site Recovery и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e6ea4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6ea4-110">PARAMETERS</span></span>

### <span data-ttu-id="e6ea4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ea4-111">-DefaultProfile</span></span>
<span data-ttu-id="e6ea4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e6ea4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e6ea4-113">-Force</span></span>
<span data-ttu-id="e6ea4-114">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="e6ea4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6ea4-115">-InputObject</span></span>
<span data-ttu-id="e6ea4-116">Входной объект для командлета: объект поставщика служб восстановления ASR, соответствующий поставщику услуг восстановления ASR, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="e6ea4-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6ea4-117">-Confirm</span></span>
<span data-ttu-id="e6ea4-118">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-118">Specify if confirmation is required.</span></span> <span data-ttu-id="e6ea4-119">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="e6ea4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ea4-120">-WhatIf</span></span>
<span data-ttu-id="e6ea4-121">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="e6ea4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ea4-122">CommonParameters</span></span>
<span data-ttu-id="e6ea4-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ea4-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6ea4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ea4-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6ea4-125">INPUTS</span></span>

### <span data-ttu-id="e6ea4-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e6ea4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="e6ea4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6ea4-127">OUTPUTS</span></span>

### <span data-ttu-id="e6ea4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e6ea4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e6ea4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6ea4-129">NOTES</span></span>

## <span data-ttu-id="e6ea4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6ea4-130">RELATED LINKS</span></span>

[<span data-ttu-id="e6ea4-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e6ea4-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="e6ea4-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e6ea4-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)