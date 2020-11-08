---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236478"
---
# <span data-ttu-id="571c1-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-101">Start-AzWebApp</span></span>

## <span data-ttu-id="571c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="571c1-102">SYNOPSIS</span></span>
<span data-ttu-id="571c1-103">Запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="571c1-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="571c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="571c1-104">SYNTAX</span></span>

### <span data-ttu-id="571c1-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="571c1-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="571c1-106">S2</span><span class="sxs-lookup"><span data-stu-id="571c1-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="571c1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="571c1-107">DESCRIPTION</span></span>
<span data-ttu-id="571c1-108">Командлет **Start-AzWebApp** запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="571c1-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="571c1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="571c1-109">EXAMPLES</span></span>

### <span data-ttu-id="571c1-110">Пример 1: запуск веб-приложения</span><span class="sxs-lookup"><span data-stu-id="571c1-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="571c1-111">Эта команда запускает веб-приложение с именем ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="571c1-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="571c1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="571c1-112">PARAMETERS</span></span>

### <span data-ttu-id="571c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571c1-113">-DefaultProfile</span></span>
<span data-ttu-id="571c1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="571c1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="571c1-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="571c1-115">-Name</span></span>
<span data-ttu-id="571c1-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-116">WebApp Name</span></span>

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

### <span data-ttu-id="571c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="571c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="571c1-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="571c1-118">Resource Group Name</span></span>

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

### <span data-ttu-id="571c1-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-119">-WebApp</span></span>
<span data-ttu-id="571c1-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-120">WebApp Object</span></span>

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

### <span data-ttu-id="571c1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571c1-121">CommonParameters</span></span>
<span data-ttu-id="571c1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="571c1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571c1-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="571c1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571c1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="571c1-124">INPUTS</span></span>

### <span data-ttu-id="571c1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="571c1-125">System.String</span></span>

### <span data-ttu-id="571c1-126">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="571c1-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="571c1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="571c1-127">OUTPUTS</span></span>

### <span data-ttu-id="571c1-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="571c1-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="571c1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="571c1-129">NOTES</span></span>

## <span data-ttu-id="571c1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="571c1-130">RELATED LINKS</span></span>

[<span data-ttu-id="571c1-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="571c1-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="571c1-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="571c1-134">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="571c1-135">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="571c1-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


