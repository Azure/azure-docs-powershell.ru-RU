---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 034736bf55eb6dc13f7ba8a51ec57da728733eb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558112"
---
# <span data-ttu-id="28171-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="28171-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="28171-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28171-102">SYNOPSIS</span></span>
<span data-ttu-id="28171-103">Запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="28171-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28171-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28171-104">SYNTAX</span></span>

### <span data-ttu-id="28171-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="28171-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28171-106">S2</span><span class="sxs-lookup"><span data-stu-id="28171-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28171-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28171-107">DESCRIPTION</span></span>
<span data-ttu-id="28171-108">Командлет **Start-AzureRmWebApp** запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="28171-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="28171-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28171-109">EXAMPLES</span></span>

### <span data-ttu-id="28171-110">Пример 1: запуск веб-приложения</span><span class="sxs-lookup"><span data-stu-id="28171-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="28171-111">Эта команда запускает веб-приложение с именем ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="28171-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="28171-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28171-112">PARAMETERS</span></span>

### <span data-ttu-id="28171-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28171-113">-DefaultProfile</span></span>
<span data-ttu-id="28171-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28171-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28171-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28171-115">-Name</span></span>
<span data-ttu-id="28171-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="28171-116">WebApp Name</span></span>

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

### <span data-ttu-id="28171-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28171-117">-ResourceGroupName</span></span>
<span data-ttu-id="28171-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="28171-118">Resource Group Name</span></span>

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

### <span data-ttu-id="28171-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="28171-119">-WebApp</span></span>
<span data-ttu-id="28171-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="28171-120">WebApp Object</span></span>

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

### <span data-ttu-id="28171-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28171-121">CommonParameters</span></span>
<span data-ttu-id="28171-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28171-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28171-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28171-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28171-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28171-124">INPUTS</span></span>

### <span data-ttu-id="28171-125">System. String</span><span class="sxs-lookup"><span data-stu-id="28171-125">System.String</span></span>

### <span data-ttu-id="28171-126">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="28171-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="28171-127">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28171-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="28171-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28171-128">OUTPUTS</span></span>

### <span data-ttu-id="28171-129">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="28171-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="28171-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="28171-130">NOTES</span></span>

## <span data-ttu-id="28171-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28171-131">RELATED LINKS</span></span>

[<span data-ttu-id="28171-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="28171-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="28171-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="28171-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="28171-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="28171-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="28171-135">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="28171-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="28171-136">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="28171-136">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


