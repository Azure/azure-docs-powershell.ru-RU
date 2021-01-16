---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326048"
---
# <span data-ttu-id="99ccf-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99ccf-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="99ccf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="99ccf-103">Перезапуск azure Web App.</span><span class="sxs-lookup"><span data-stu-id="99ccf-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="99ccf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99ccf-104">SYNTAX</span></span>

### <span data-ttu-id="99ccf-105">S1</span><span class="sxs-lookup"><span data-stu-id="99ccf-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99ccf-106">S2</span><span class="sxs-lookup"><span data-stu-id="99ccf-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99ccf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99ccf-107">DESCRIPTION</span></span>
<span data-ttu-id="99ccf-108">Запуск веб-приложения Azure Web App прекращается с помощью **cmdlet Restart-AzWebApp.**</span><span class="sxs-lookup"><span data-stu-id="99ccf-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="99ccf-109">Если состояние веб-приложения остановлено, используйте Start-AzWebApp управления.</span><span class="sxs-lookup"><span data-stu-id="99ccf-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="99ccf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99ccf-110">EXAMPLES</span></span>

### <span data-ttu-id="99ccf-111">Пример 1. Перезапуск веб-приложения</span><span class="sxs-lookup"><span data-stu-id="99ccf-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="99ccf-112">Эта команда останавливает Azure Web App ContosoSite, которая принадлежит к группе ресурсов Default-Web-WestUS, и перезапускает ее.</span><span class="sxs-lookup"><span data-stu-id="99ccf-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="99ccf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99ccf-113">PARAMETERS</span></span>

### <span data-ttu-id="99ccf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ccf-114">-DefaultProfile</span></span>
<span data-ttu-id="99ccf-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99ccf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99ccf-116">-Name</span><span class="sxs-lookup"><span data-stu-id="99ccf-116">-Name</span></span>
<span data-ttu-id="99ccf-117">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="99ccf-117">WebApp Name</span></span>

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

### <span data-ttu-id="99ccf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ccf-118">-ResourceGroupName</span></span>
<span data-ttu-id="99ccf-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="99ccf-119">Resource Group Name</span></span>

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

### <span data-ttu-id="99ccf-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="99ccf-120">-WebApp</span></span>
<span data-ttu-id="99ccf-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="99ccf-121">WebApp Object</span></span>

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

### <span data-ttu-id="99ccf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ccf-122">CommonParameters</span></span>
<span data-ttu-id="99ccf-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ccf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ccf-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99ccf-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ccf-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99ccf-125">INPUTS</span></span>

### <span data-ttu-id="99ccf-126">System.String</span><span class="sxs-lookup"><span data-stu-id="99ccf-126">System.String</span></span>

### <span data-ttu-id="99ccf-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="99ccf-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="99ccf-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99ccf-128">OUTPUTS</span></span>

### <span data-ttu-id="99ccf-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="99ccf-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="99ccf-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99ccf-130">NOTES</span></span>

## <span data-ttu-id="99ccf-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99ccf-131">RELATED LINKS</span></span>

[<span data-ttu-id="99ccf-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99ccf-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="99ccf-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99ccf-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="99ccf-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99ccf-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="99ccf-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99ccf-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="99ccf-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99ccf-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


