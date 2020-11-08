---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249170"
---
# <span data-ttu-id="3db56-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3db56-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="3db56-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3db56-102">SYNOPSIS</span></span>
<span data-ttu-id="3db56-103">Обновляет (обновить сервер) данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3db56-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="3db56-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3db56-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3db56-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3db56-105">DESCRIPTION</span></span>
<span data-ttu-id="3db56-106">Командлет **Update-AzRecoveryServicesAsrServicesProvider** обновляет данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3db56-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="3db56-107">Этот командлет можно использовать для активации обновления данных, полученных от поставщика услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="3db56-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="3db56-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3db56-108">EXAMPLES</span></span>

### <span data-ttu-id="3db56-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3db56-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="3db56-110">Запускает операцию обновления данных, предоставленных указанным поставщиком служб ASR, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="3db56-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3db56-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3db56-111">PARAMETERS</span></span>

### <span data-ttu-id="3db56-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db56-112">-DefaultProfile</span></span>
<span data-ttu-id="3db56-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3db56-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3db56-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3db56-114">-InputObject</span></span>
<span data-ttu-id="3db56-115">Указывает объект поставщика служб ASR, который определяет сервер, сведения о котором нужно обновить (обновление.)</span><span class="sxs-lookup"><span data-stu-id="3db56-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="3db56-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3db56-116">-Confirm</span></span>
<span data-ttu-id="3db56-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3db56-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db56-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db56-118">-WhatIf</span></span>
<span data-ttu-id="3db56-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3db56-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3db56-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3db56-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db56-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db56-121">CommonParameters</span></span>
<span data-ttu-id="3db56-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3db56-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db56-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3db56-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db56-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3db56-124">INPUTS</span></span>

### <span data-ttu-id="3db56-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3db56-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="3db56-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3db56-126">OUTPUTS</span></span>

### <span data-ttu-id="3db56-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3db56-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3db56-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3db56-128">NOTES</span></span>

## <span data-ttu-id="3db56-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3db56-129">RELATED LINKS</span></span>

[<span data-ttu-id="3db56-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3db56-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="3db56-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3db56-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
