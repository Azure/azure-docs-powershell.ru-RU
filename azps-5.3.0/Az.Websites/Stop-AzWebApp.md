---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505718"
---
# <span data-ttu-id="008ac-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="008ac-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="008ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="008ac-102">SYNOPSIS</span></span>
<span data-ttu-id="008ac-103">Остановка Службы Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="008ac-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="008ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="008ac-104">SYNTAX</span></span>

### <span data-ttu-id="008ac-105">S1</span><span class="sxs-lookup"><span data-stu-id="008ac-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="008ac-106">S2</span><span class="sxs-lookup"><span data-stu-id="008ac-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="008ac-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="008ac-107">DESCRIPTION</span></span>
<span data-ttu-id="008ac-108">С **помощью cmdlet Stop-AzWebApp** можно прекратить работу Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="008ac-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="008ac-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="008ac-109">EXAMPLES</span></span>

### <span data-ttu-id="008ac-110">Пример 1. Остановка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="008ac-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="008ac-111">Эта команда останавливает веб-приложение ContosoWebApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="008ac-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="008ac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="008ac-112">PARAMETERS</span></span>

### <span data-ttu-id="008ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008ac-113">-DefaultProfile</span></span>
<span data-ttu-id="008ac-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="008ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="008ac-115">-Name</span><span class="sxs-lookup"><span data-stu-id="008ac-115">-Name</span></span>
<span data-ttu-id="008ac-116">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="008ac-116">WebApp Name</span></span>

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

### <span data-ttu-id="008ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="008ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="008ac-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="008ac-118">Resource Group Name</span></span>

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

### <span data-ttu-id="008ac-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="008ac-119">-WebApp</span></span>
<span data-ttu-id="008ac-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="008ac-120">WebApp Object</span></span>

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

### <span data-ttu-id="008ac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008ac-121">CommonParameters</span></span>
<span data-ttu-id="008ac-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008ac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008ac-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="008ac-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008ac-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="008ac-124">INPUTS</span></span>

### <span data-ttu-id="008ac-125">System.String</span><span class="sxs-lookup"><span data-stu-id="008ac-125">System.String</span></span>

### <span data-ttu-id="008ac-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="008ac-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="008ac-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="008ac-127">OUTPUTS</span></span>

### <span data-ttu-id="008ac-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="008ac-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="008ac-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="008ac-129">NOTES</span></span>

## <span data-ttu-id="008ac-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="008ac-130">RELATED LINKS</span></span>

[<span data-ttu-id="008ac-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="008ac-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="008ac-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="008ac-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="008ac-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="008ac-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="008ac-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="008ac-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="008ac-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="008ac-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


