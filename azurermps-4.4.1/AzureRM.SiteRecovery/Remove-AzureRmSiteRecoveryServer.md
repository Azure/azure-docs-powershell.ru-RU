---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 4be04d590adbf75760472f4047b7de9efcffd2d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734768"
---
# <span data-ttu-id="63060-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="63060-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="63060-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63060-102">SYNOPSIS</span></span>
<span data-ttu-id="63060-103">Удаление сервера восстановления сайта из текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="63060-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63060-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63060-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63060-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63060-105">DESCRIPTION</span></span>
<span data-ttu-id="63060-106">Командлет **Remove-AzureRmSiteRecoveryServer** отменяет регистрацию сервера Azure Site Recovery, который удаляет его из текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="63060-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="63060-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63060-107">EXAMPLES</span></span>

## <span data-ttu-id="63060-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63060-108">PARAMETERS</span></span>

### <span data-ttu-id="63060-109">-Force</span><span class="sxs-lookup"><span data-stu-id="63060-109">-Force</span></span>
<span data-ttu-id="63060-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="63060-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63060-111">-Сервер</span><span class="sxs-lookup"><span data-stu-id="63060-111">-Server</span></span>
<span data-ttu-id="63060-112">Указывает объект сервера восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="63060-112">Specifies the Site Recovery server object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63060-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63060-113">-Confirm</span></span>
<span data-ttu-id="63060-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63060-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63060-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63060-115">-WhatIf</span></span>
<span data-ttu-id="63060-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63060-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="63060-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63060-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63060-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63060-118">-DefaultProfile</span></span>
<span data-ttu-id="63060-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63060-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63060-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63060-120">CommonParameters</span></span>
<span data-ttu-id="63060-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63060-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63060-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63060-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63060-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63060-123">INPUTS</span></span>

### <span data-ttu-id="63060-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="63060-124">ASRServer</span></span>
<span data-ttu-id="63060-125">Параметр Server принимает значение типа "ASRServer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="63060-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="63060-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63060-126">OUTPUTS</span></span>

### <span data-ttu-id="63060-127">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="63060-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="63060-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="63060-128">NOTES</span></span>

## <span data-ttu-id="63060-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63060-129">RELATED LINKS</span></span>

[<span data-ttu-id="63060-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="63060-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="63060-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="63060-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
