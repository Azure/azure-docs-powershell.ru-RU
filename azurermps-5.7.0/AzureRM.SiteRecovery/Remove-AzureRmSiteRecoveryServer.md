---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 7c7afc0a1b6544f165f379a7363960142f73780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733960"
---
# <span data-ttu-id="649dc-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="649dc-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="649dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="649dc-102">SYNOPSIS</span></span>
<span data-ttu-id="649dc-103">Удаление сервера восстановления сайта из текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="649dc-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="649dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="649dc-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="649dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="649dc-105">DESCRIPTION</span></span>
<span data-ttu-id="649dc-106">Командлет **Remove-AzureRmSiteRecoveryServer** отменяет регистрацию сервера Azure Site Recovery, который удаляет его из текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="649dc-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="649dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="649dc-107">EXAMPLES</span></span>

## <span data-ttu-id="649dc-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="649dc-108">PARAMETERS</span></span>

### <span data-ttu-id="649dc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="649dc-109">-DefaultProfile</span></span>
<span data-ttu-id="649dc-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="649dc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="649dc-111">-Force</span><span class="sxs-lookup"><span data-stu-id="649dc-111">-Force</span></span>
<span data-ttu-id="649dc-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="649dc-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="649dc-113">-Сервер</span><span class="sxs-lookup"><span data-stu-id="649dc-113">-Server</span></span>
<span data-ttu-id="649dc-114">Указывает объект сервера восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="649dc-114">Specifies the Site Recovery server object.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="649dc-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="649dc-115">-Confirm</span></span>
<span data-ttu-id="649dc-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="649dc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="649dc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="649dc-117">-WhatIf</span></span>
<span data-ttu-id="649dc-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="649dc-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="649dc-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="649dc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="649dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="649dc-120">CommonParameters</span></span>
<span data-ttu-id="649dc-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="649dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="649dc-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="649dc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="649dc-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="649dc-123">INPUTS</span></span>

### <span data-ttu-id="649dc-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="649dc-124">ASRServer</span></span>
<span data-ttu-id="649dc-125">Параметр Server принимает значение типа "ASRServer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="649dc-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="649dc-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="649dc-126">OUTPUTS</span></span>

### <span data-ttu-id="649dc-127">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="649dc-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="649dc-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="649dc-128">NOTES</span></span>

## <span data-ttu-id="649dc-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="649dc-129">RELATED LINKS</span></span>

[<span data-ttu-id="649dc-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="649dc-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="649dc-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="649dc-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
