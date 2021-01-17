---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422620"
---
# <span data-ttu-id="85539-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="85539-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="85539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85539-102">SYNOPSIS</span></span>
<span data-ttu-id="85539-103">Get-AzWebAppContainerContinuousDeploymentUrl возвращает URL-адрес непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="85539-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="85539-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85539-104">SYNTAX</span></span>

### <span data-ttu-id="85539-105">S1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85539-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85539-106">S2</span><span class="sxs-lookup"><span data-stu-id="85539-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85539-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85539-107">DESCRIPTION</span></span>
<span data-ttu-id="85539-108">Get-AzWebAppContainerContinuousDeploymentUrl возвращает URL-адрес непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="85539-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="85539-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85539-109">EXAMPLES</span></span>

### <span data-ttu-id="85539-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85539-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="85539-111">Эта команда возвращает URL-адрес непрерывного развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="85539-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="85539-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85539-112">PARAMETERS</span></span>

### <span data-ttu-id="85539-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85539-113">-DefaultProfile</span></span>
<span data-ttu-id="85539-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85539-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85539-115">-Name</span><span class="sxs-lookup"><span data-stu-id="85539-115">-Name</span></span>
<span data-ttu-id="85539-116">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="85539-116">The name of the web app.</span></span>

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

### <span data-ttu-id="85539-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85539-117">-ResourceGroupName</span></span>
<span data-ttu-id="85539-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85539-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="85539-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="85539-119">-SlotName</span></span>
<span data-ttu-id="85539-120">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="85539-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85539-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="85539-121">-WebApp</span></span>
<span data-ttu-id="85539-122">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="85539-122">The web app object</span></span>

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

### <span data-ttu-id="85539-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85539-123">CommonParameters</span></span>
<span data-ttu-id="85539-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85539-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85539-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85539-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85539-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85539-126">INPUTS</span></span>

### <span data-ttu-id="85539-127">System.String</span><span class="sxs-lookup"><span data-stu-id="85539-127">System.String</span></span>

### <span data-ttu-id="85539-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="85539-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="85539-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85539-129">OUTPUTS</span></span>

### <span data-ttu-id="85539-130">System.String</span><span class="sxs-lookup"><span data-stu-id="85539-130">System.String</span></span>

## <span data-ttu-id="85539-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85539-131">NOTES</span></span>

## <span data-ttu-id="85539-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85539-132">RELATED LINKS</span></span>
