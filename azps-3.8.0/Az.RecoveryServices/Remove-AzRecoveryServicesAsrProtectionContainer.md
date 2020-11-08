---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072640"
---
# <span data-ttu-id="23bcf-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="23bcf-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="23bcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="23bcf-103">Удаляет указанный контейнер защиты из его структуры.</span><span class="sxs-lookup"><span data-stu-id="23bcf-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="23bcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23bcf-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23bcf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="23bcf-106">Командлет Remove-AzRecoveryServicesAsrProtectionContainer удаляет указанный контейнер защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="23bcf-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="23bcf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23bcf-107">EXAMPLES</span></span>

### <span data-ttu-id="23bcf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23bcf-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="23bcf-109">Запускает удаление указанного контейнера защиты и возвращает задание ASR, используемое для отслеживания операции удаления.</span><span class="sxs-lookup"><span data-stu-id="23bcf-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="23bcf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23bcf-110">PARAMETERS</span></span>

### <span data-ttu-id="23bcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23bcf-111">-DefaultProfile</span></span>
<span data-ttu-id="23bcf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23bcf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23bcf-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23bcf-113">-InputObject</span></span>
<span data-ttu-id="23bcf-114">Указывает контейнер защиты, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="23bcf-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="23bcf-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23bcf-115">-Confirm</span></span>
<span data-ttu-id="23bcf-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="23bcf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23bcf-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23bcf-117">-WhatIf</span></span>
<span data-ttu-id="23bcf-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="23bcf-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23bcf-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23bcf-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23bcf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23bcf-120">CommonParameters</span></span>
<span data-ttu-id="23bcf-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23bcf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23bcf-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23bcf-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23bcf-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23bcf-123">INPUTS</span></span>

### <span data-ttu-id="23bcf-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="23bcf-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="23bcf-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23bcf-125">OUTPUTS</span></span>

### <span data-ttu-id="23bcf-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="23bcf-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="23bcf-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="23bcf-127">NOTES</span></span>

## <span data-ttu-id="23bcf-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23bcf-128">RELATED LINKS</span></span>
