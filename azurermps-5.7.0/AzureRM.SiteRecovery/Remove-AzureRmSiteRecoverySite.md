---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: a83b4b8ca3dbe415013fe9a858d46cb886ce4b00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557147"
---
# <span data-ttu-id="b276a-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="b276a-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="b276a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b276a-102">SYNOPSIS</span></span>
<span data-ttu-id="b276a-103">Удаляет сайт восстановления сайта из текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b276a-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b276a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b276a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b276a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b276a-105">DESCRIPTION</span></span>
<span data-ttu-id="b276a-106">Командлет **Remove-AzureRmSiteRecoverySite** удаляет сайт Azure Site Recovery из текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b276a-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="b276a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b276a-107">EXAMPLES</span></span>

## <span data-ttu-id="b276a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b276a-108">PARAMETERS</span></span>

### <span data-ttu-id="b276a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b276a-109">-DefaultProfile</span></span>
<span data-ttu-id="b276a-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b276a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b276a-111">-Force</span></span>
<span data-ttu-id="b276a-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b276a-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-113">-Site</span><span class="sxs-lookup"><span data-stu-id="b276a-113">-Site</span></span>
<span data-ttu-id="b276a-114">Указывает объект сайта для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="b276a-114">Specifies the Site Recovery site object.</span></span>

```yaml
Type: ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b276a-115">-Confirm</span></span>
<span data-ttu-id="b276a-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b276a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b276a-117">-WhatIf</span></span>
<span data-ttu-id="b276a-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b276a-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b276a-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b276a-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b276a-120">CommonParameters</span></span>
<span data-ttu-id="b276a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b276a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b276a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b276a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b276a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b276a-123">INPUTS</span></span>

### <span data-ttu-id="b276a-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="b276a-124">ASRSite</span></span>
<span data-ttu-id="b276a-125">Параметр "сайт" принимает значение типа "ASRSite" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b276a-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="b276a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b276a-126">OUTPUTS</span></span>

## <span data-ttu-id="b276a-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b276a-127">NOTES</span></span>

## <span data-ttu-id="b276a-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b276a-128">RELATED LINKS</span></span>

[<span data-ttu-id="b276a-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="b276a-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="b276a-130">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="b276a-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
