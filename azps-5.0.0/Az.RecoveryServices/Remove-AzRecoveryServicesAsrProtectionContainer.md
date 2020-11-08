---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248041"
---
# <span data-ttu-id="c06a4-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c06a4-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c06a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c06a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c06a4-103">Удаляет указанный контейнер защиты из его структуры.</span><span class="sxs-lookup"><span data-stu-id="c06a4-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="c06a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c06a4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c06a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c06a4-105">DESCRIPTION</span></span>
<span data-ttu-id="c06a4-106">Командлет Remove-AzRecoveryServicesAsrProtectionContainer удаляет указанный контейнер защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c06a4-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="c06a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c06a4-107">EXAMPLES</span></span>

### <span data-ttu-id="c06a4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c06a4-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="c06a4-109">Запускает удаление указанного контейнера защиты и возвращает задание ASR, используемое для отслеживания операции удаления.</span><span class="sxs-lookup"><span data-stu-id="c06a4-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="c06a4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c06a4-110">PARAMETERS</span></span>

### <span data-ttu-id="c06a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06a4-111">-DefaultProfile</span></span>
<span data-ttu-id="c06a4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c06a4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c06a4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c06a4-113">-InputObject</span></span>
<span data-ttu-id="c06a4-114">Указывает контейнер защиты, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c06a4-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c06a4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c06a4-115">-Confirm</span></span>
<span data-ttu-id="c06a4-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c06a4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c06a4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c06a4-117">-WhatIf</span></span>
<span data-ttu-id="c06a4-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c06a4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c06a4-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c06a4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c06a4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06a4-120">CommonParameters</span></span>
<span data-ttu-id="c06a4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c06a4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06a4-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c06a4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06a4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c06a4-123">INPUTS</span></span>

### <span data-ttu-id="c06a4-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c06a4-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c06a4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c06a4-125">OUTPUTS</span></span>

### <span data-ttu-id="c06a4-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c06a4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c06a4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c06a4-127">NOTES</span></span>

## <span data-ttu-id="c06a4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c06a4-128">RELATED LINKS</span></span>
