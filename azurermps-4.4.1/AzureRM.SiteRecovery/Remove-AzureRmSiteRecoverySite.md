---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: f052b11a11fa77047d424b7045b127a75043cc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733316"
---
# <span data-ttu-id="c4fd7-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="c4fd7-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="c4fd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fd7-103">Удаляет сайт восстановления сайта из текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4fd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4fd7-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4fd7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="c4fd7-106">Командлет **Remove-AzureRmSiteRecoverySite** удаляет сайт Azure Site Recovery из текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="c4fd7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4fd7-107">EXAMPLES</span></span>

## <span data-ttu-id="c4fd7-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4fd7-108">PARAMETERS</span></span>

### <span data-ttu-id="c4fd7-109">-Force</span><span class="sxs-lookup"><span data-stu-id="c4fd7-109">-Force</span></span>
<span data-ttu-id="c4fd7-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4fd7-111">-Site</span><span class="sxs-lookup"><span data-stu-id="c4fd7-111">-Site</span></span>
<span data-ttu-id="c4fd7-112">Указывает объект сайта для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-112">Specifies the Site Recovery site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd7-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4fd7-113">-Confirm</span></span>
<span data-ttu-id="c4fd7-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd7-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4fd7-115">-WhatIf</span></span>
<span data-ttu-id="c4fd7-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c4fd7-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fd7-118">-DefaultProfile</span></span>
<span data-ttu-id="c4fd7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fd7-120">CommonParameters</span></span>
<span data-ttu-id="c4fd7-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fd7-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4fd7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fd7-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4fd7-123">INPUTS</span></span>

### <span data-ttu-id="c4fd7-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="c4fd7-124">ASRSite</span></span>
<span data-ttu-id="c4fd7-125">Параметр "сайт" принимает значение типа "ASRSite" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c4fd7-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="c4fd7-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4fd7-126">OUTPUTS</span></span>

## <span data-ttu-id="c4fd7-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4fd7-127">NOTES</span></span>

## <span data-ttu-id="c4fd7-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4fd7-128">RELATED LINKS</span></span>

[<span data-ttu-id="c4fd7-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="c4fd7-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="c4fd7-130">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="c4fd7-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
