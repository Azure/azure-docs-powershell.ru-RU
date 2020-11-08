---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244651"
---
# <span data-ttu-id="951ab-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="951ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="951ab-102">SYNOPSIS</span></span>
<span data-ttu-id="951ab-103">Останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="951ab-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="951ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="951ab-104">SYNTAX</span></span>

### <span data-ttu-id="951ab-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="951ab-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="951ab-106">S2</span><span class="sxs-lookup"><span data-stu-id="951ab-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="951ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="951ab-107">DESCRIPTION</span></span>
<span data-ttu-id="951ab-108">Командлет **Stop-AzWebApp** останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="951ab-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="951ab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="951ab-109">EXAMPLES</span></span>

### <span data-ttu-id="951ab-110">Пример 1: остановка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="951ab-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="951ab-111">Эта команда останавливает веб-приложение ContosoWebApp, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="951ab-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="951ab-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="951ab-112">PARAMETERS</span></span>

### <span data-ttu-id="951ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951ab-113">-DefaultProfile</span></span>
<span data-ttu-id="951ab-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="951ab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="951ab-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="951ab-115">-Name</span></span>
<span data-ttu-id="951ab-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-116">WebApp Name</span></span>

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

### <span data-ttu-id="951ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="951ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="951ab-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="951ab-118">Resource Group Name</span></span>

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

### <span data-ttu-id="951ab-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-119">-WebApp</span></span>
<span data-ttu-id="951ab-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-120">WebApp Object</span></span>

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

### <span data-ttu-id="951ab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951ab-121">CommonParameters</span></span>
<span data-ttu-id="951ab-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="951ab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951ab-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="951ab-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951ab-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="951ab-124">INPUTS</span></span>

### <span data-ttu-id="951ab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="951ab-125">System.String</span></span>

### <span data-ttu-id="951ab-126">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="951ab-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="951ab-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="951ab-127">OUTPUTS</span></span>

### <span data-ttu-id="951ab-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="951ab-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="951ab-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="951ab-129">NOTES</span></span>

## <span data-ttu-id="951ab-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="951ab-130">RELATED LINKS</span></span>

[<span data-ttu-id="951ab-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="951ab-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="951ab-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="951ab-134">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="951ab-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="951ab-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


