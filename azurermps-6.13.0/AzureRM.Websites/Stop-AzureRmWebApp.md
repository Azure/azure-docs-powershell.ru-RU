---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: b389a84ea57902e2e7a7dabaea2d853827a728e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558108"
---
# <span data-ttu-id="92e50-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="92e50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92e50-102">SYNOPSIS</span></span>
<span data-ttu-id="92e50-103">Останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="92e50-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92e50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92e50-104">SYNTAX</span></span>

### <span data-ttu-id="92e50-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="92e50-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92e50-106">S2</span><span class="sxs-lookup"><span data-stu-id="92e50-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e50-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92e50-107">DESCRIPTION</span></span>
<span data-ttu-id="92e50-108">Командлет **Stop-AzureRmWebApp** останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="92e50-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="92e50-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92e50-109">EXAMPLES</span></span>

### <span data-ttu-id="92e50-110">Пример 1: остановка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="92e50-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="92e50-111">Эта команда останавливает веб-приложение ContosoWebApp, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="92e50-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="92e50-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92e50-112">PARAMETERS</span></span>

### <span data-ttu-id="92e50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e50-113">-DefaultProfile</span></span>
<span data-ttu-id="92e50-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92e50-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92e50-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92e50-115">-Name</span></span>
<span data-ttu-id="92e50-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e50-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e50-117">-ResourceGroupName</span></span>
<span data-ttu-id="92e50-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="92e50-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e50-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-119">-WebApp</span></span>
<span data-ttu-id="92e50-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92e50-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e50-121">CommonParameters</span></span>
<span data-ttu-id="92e50-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92e50-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e50-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e50-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e50-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92e50-124">INPUTS</span></span>

### <span data-ttu-id="92e50-125">System. String</span><span class="sxs-lookup"><span data-stu-id="92e50-125">System.String</span></span>

### <span data-ttu-id="92e50-126">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="92e50-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="92e50-127">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92e50-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="92e50-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92e50-128">OUTPUTS</span></span>

### <span data-ttu-id="92e50-129">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="92e50-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="92e50-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="92e50-130">NOTES</span></span>

## <span data-ttu-id="92e50-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92e50-131">RELATED LINKS</span></span>

[<span data-ttu-id="92e50-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="92e50-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="92e50-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="92e50-135">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="92e50-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92e50-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


