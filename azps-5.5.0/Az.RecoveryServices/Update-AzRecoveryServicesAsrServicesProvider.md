---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217908"
---
# <span data-ttu-id="c496f-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c496f-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="c496f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c496f-102">SYNOPSIS</span></span>
<span data-ttu-id="c496f-103">Обновление (сервер обновления) информации, полученной от поставщика служб восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="c496f-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="c496f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c496f-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c496f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c496f-105">DESCRIPTION</span></span>
<span data-ttu-id="c496f-106">При этом сведения, полученные от поставщика услуг восстановления сайта Azure, обновляются с использованием **cmdlet Update-AzRecoveryServicesAsrServicesProvider.**</span><span class="sxs-lookup"><span data-stu-id="c496f-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="c496f-107">С помощью этого cmdlet можно обновить сведения, полученные от поставщика услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="c496f-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="c496f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c496f-108">EXAMPLES</span></span>

### <span data-ttu-id="c496f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c496f-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="c496f-110">Начинает обновление сведений от указанного поставщика служб ASR и возвращает задание ASR, используемое для ее отслеживания.</span><span class="sxs-lookup"><span data-stu-id="c496f-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c496f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c496f-111">PARAMETERS</span></span>

### <span data-ttu-id="c496f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c496f-112">-DefaultProfile</span></span>
<span data-ttu-id="c496f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c496f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c496f-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c496f-114">-InputObject</span></span>
<span data-ttu-id="c496f-115">Определяет объект поставщика служб ASR, определя который определяет сервер, для которого требуется обновить (обновленную) информацию.</span><span class="sxs-lookup"><span data-stu-id="c496f-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="c496f-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c496f-116">-Confirm</span></span>
<span data-ttu-id="c496f-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c496f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c496f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c496f-118">-WhatIf</span></span>
<span data-ttu-id="c496f-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c496f-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c496f-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c496f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c496f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c496f-121">CommonParameters</span></span>
<span data-ttu-id="c496f-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c496f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c496f-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c496f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c496f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c496f-124">INPUTS</span></span>

### <span data-ttu-id="c496f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c496f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="c496f-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c496f-126">OUTPUTS</span></span>

### <span data-ttu-id="c496f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c496f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c496f-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c496f-128">NOTES</span></span>

## <span data-ttu-id="c496f-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c496f-129">RELATED LINKS</span></span>

[<span data-ttu-id="c496f-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c496f-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="c496f-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c496f-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
