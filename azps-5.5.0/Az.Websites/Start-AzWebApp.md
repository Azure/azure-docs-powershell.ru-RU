---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222740"
---
# <span data-ttu-id="98c0a-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="98c0a-101">Start-AzWebApp</span></span>

## <span data-ttu-id="98c0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="98c0a-103">Запускает Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="98c0a-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="98c0a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98c0a-104">SYNTAX</span></span>

### <span data-ttu-id="98c0a-105">S1</span><span class="sxs-lookup"><span data-stu-id="98c0a-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98c0a-106">S2</span><span class="sxs-lookup"><span data-stu-id="98c0a-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c0a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c0a-107">DESCRIPTION</span></span>
<span data-ttu-id="98c0a-108">Для **запуска Azure Web App запускается cmdlet Start-AzWebApp.**</span><span class="sxs-lookup"><span data-stu-id="98c0a-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="98c0a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98c0a-109">EXAMPLES</span></span>

### <span data-ttu-id="98c0a-110">Пример 1. Запуск веб-приложения</span><span class="sxs-lookup"><span data-stu-id="98c0a-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="98c0a-111">Эта команда запускает веб-приложение ContosoWebApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="98c0a-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="98c0a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98c0a-112">PARAMETERS</span></span>

### <span data-ttu-id="98c0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c0a-113">-DefaultProfile</span></span>
<span data-ttu-id="98c0a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98c0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98c0a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="98c0a-115">-Name</span></span>
<span data-ttu-id="98c0a-116">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="98c0a-116">WebApp Name</span></span>

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

### <span data-ttu-id="98c0a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c0a-117">-ResourceGroupName</span></span>
<span data-ttu-id="98c0a-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="98c0a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="98c0a-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="98c0a-119">-WebApp</span></span>
<span data-ttu-id="98c0a-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="98c0a-120">WebApp Object</span></span>

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

### <span data-ttu-id="98c0a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c0a-121">CommonParameters</span></span>
<span data-ttu-id="98c0a-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c0a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c0a-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c0a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c0a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98c0a-124">INPUTS</span></span>

### <span data-ttu-id="98c0a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="98c0a-125">System.String</span></span>

### <span data-ttu-id="98c0a-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="98c0a-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="98c0a-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98c0a-127">OUTPUTS</span></span>

### <span data-ttu-id="98c0a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="98c0a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="98c0a-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98c0a-129">NOTES</span></span>

## <span data-ttu-id="98c0a-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98c0a-130">RELATED LINKS</span></span>

[<span data-ttu-id="98c0a-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="98c0a-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="98c0a-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="98c0a-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="98c0a-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="98c0a-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="98c0a-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="98c0a-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="98c0a-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="98c0a-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


