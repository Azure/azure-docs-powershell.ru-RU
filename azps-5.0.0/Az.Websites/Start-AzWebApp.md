---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247969"
---
# <span data-ttu-id="6ffe5-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-101">Start-AzWebApp</span></span>

## <span data-ttu-id="6ffe5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ffe5-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffe5-103">Запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffe5-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="6ffe5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ffe5-104">SYNTAX</span></span>

### <span data-ttu-id="6ffe5-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="6ffe5-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ffe5-106">S2</span><span class="sxs-lookup"><span data-stu-id="6ffe5-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ffe5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ffe5-107">DESCRIPTION</span></span>
<span data-ttu-id="6ffe5-108">Командлет **Start-AzWebApp** запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffe5-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="6ffe5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ffe5-109">EXAMPLES</span></span>

### <span data-ttu-id="6ffe5-110">Пример 1: запуск веб-приложения</span><span class="sxs-lookup"><span data-stu-id="6ffe5-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="6ffe5-111">Эта команда запускает веб-приложение с именем ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6ffe5-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6ffe5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ffe5-112">PARAMETERS</span></span>

### <span data-ttu-id="6ffe5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffe5-113">-DefaultProfile</span></span>
<span data-ttu-id="6ffe5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffe5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ffe5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6ffe5-115">-Name</span></span>
<span data-ttu-id="6ffe5-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-116">WebApp Name</span></span>

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

### <span data-ttu-id="6ffe5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffe5-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ffe5-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ffe5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6ffe5-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-119">-WebApp</span></span>
<span data-ttu-id="6ffe5-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-120">WebApp Object</span></span>

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

### <span data-ttu-id="6ffe5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffe5-121">CommonParameters</span></span>
<span data-ttu-id="6ffe5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ffe5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffe5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ffe5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffe5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ffe5-124">INPUTS</span></span>

### <span data-ttu-id="6ffe5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffe5-125">System.String</span></span>

### <span data-ttu-id="6ffe5-126">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="6ffe5-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6ffe5-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ffe5-127">OUTPUTS</span></span>

### <span data-ttu-id="6ffe5-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="6ffe5-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6ffe5-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ffe5-129">NOTES</span></span>

## <span data-ttu-id="6ffe5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ffe5-130">RELATED LINKS</span></span>

[<span data-ttu-id="6ffe5-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="6ffe5-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="6ffe5-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="6ffe5-134">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="6ffe5-135">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6ffe5-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

