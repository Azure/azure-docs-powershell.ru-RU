---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401652"
---
# <span data-ttu-id="4ba93-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4ba93-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="4ba93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ba93-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba93-103">Обновление (сервер обновления) информации, полученной от поставщика служб восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba93-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="4ba93-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ba93-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ba93-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba93-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba93-106">При этом сведения, полученные от поставщика услуг восстановления сайта Azure, обновляются с использованием **cmdlet Update-AzRecoveryServicesAsrServicesProvider.**</span><span class="sxs-lookup"><span data-stu-id="4ba93-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="4ba93-107">С помощью этого cmdlet вы можете обновить данные, полученные от поставщика услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="4ba93-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="4ba93-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ba93-108">EXAMPLES</span></span>

### <span data-ttu-id="4ba93-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ba93-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="4ba93-110">Запускает операцию обновления сведений от указанного поставщика служб ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="4ba93-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4ba93-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ba93-111">PARAMETERS</span></span>

### <span data-ttu-id="4ba93-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba93-112">-DefaultProfile</span></span>
<span data-ttu-id="4ba93-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba93-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4ba93-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba93-114">-InputObject</span></span>
<span data-ttu-id="4ba93-115">Определяет объект поставщика служб ASR, определя который определяет сервер, для которого требуется обновить (обновленную) информацию.</span><span class="sxs-lookup"><span data-stu-id="4ba93-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="4ba93-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ba93-116">-Confirm</span></span>
<span data-ttu-id="4ba93-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ba93-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba93-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba93-118">-WhatIf</span></span>
<span data-ttu-id="4ba93-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ba93-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ba93-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ba93-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba93-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba93-121">CommonParameters</span></span>
<span data-ttu-id="4ba93-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ba93-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba93-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ba93-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba93-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ba93-124">INPUTS</span></span>

### <span data-ttu-id="4ba93-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4ba93-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="4ba93-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ba93-126">OUTPUTS</span></span>

### <span data-ttu-id="4ba93-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4ba93-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4ba93-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ba93-128">NOTES</span></span>

## <span data-ttu-id="4ba93-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ba93-129">RELATED LINKS</span></span>

[<span data-ttu-id="4ba93-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4ba93-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="4ba93-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4ba93-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
