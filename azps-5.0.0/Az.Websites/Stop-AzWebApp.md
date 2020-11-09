---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318749"
---
# <span data-ttu-id="a0ed8-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="a0ed8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ed8-103">Останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ed8-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="a0ed8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0ed8-104">SYNTAX</span></span>

### <span data-ttu-id="a0ed8-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="a0ed8-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0ed8-106">S2</span><span class="sxs-lookup"><span data-stu-id="a0ed8-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0ed8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="a0ed8-108">Командлет **Stop-AzWebApp** останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ed8-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="a0ed8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0ed8-109">EXAMPLES</span></span>

### <span data-ttu-id="a0ed8-110">Пример 1: остановка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="a0ed8-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a0ed8-111">Эта команда останавливает веб-приложение ContosoWebApp, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a0ed8-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a0ed8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0ed8-112">PARAMETERS</span></span>

### <span data-ttu-id="a0ed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ed8-113">-DefaultProfile</span></span>
<span data-ttu-id="a0ed8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ed8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0ed8-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a0ed8-115">-Name</span></span>
<span data-ttu-id="a0ed8-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-116">WebApp Name</span></span>

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

### <span data-ttu-id="a0ed8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ed8-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0ed8-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a0ed8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a0ed8-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-119">-WebApp</span></span>
<span data-ttu-id="a0ed8-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-120">WebApp Object</span></span>

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

### <span data-ttu-id="a0ed8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ed8-121">CommonParameters</span></span>
<span data-ttu-id="a0ed8-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0ed8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ed8-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0ed8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ed8-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0ed8-124">INPUTS</span></span>

### <span data-ttu-id="a0ed8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a0ed8-125">System.String</span></span>

### <span data-ttu-id="a0ed8-126">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="a0ed8-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a0ed8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0ed8-127">OUTPUTS</span></span>

### <span data-ttu-id="a0ed8-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="a0ed8-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a0ed8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0ed8-129">NOTES</span></span>

## <span data-ttu-id="a0ed8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0ed8-130">RELATED LINKS</span></span>

[<span data-ttu-id="a0ed8-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a0ed8-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a0ed8-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a0ed8-134">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a0ed8-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a0ed8-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


