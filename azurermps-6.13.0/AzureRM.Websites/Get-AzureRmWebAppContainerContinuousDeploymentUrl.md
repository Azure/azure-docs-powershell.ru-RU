---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 0618b7c4cc4f9ee8b2342306e4aadf83ff0c17f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563920"
---
# <span data-ttu-id="88e92-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="88e92-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="88e92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88e92-102">SYNOPSIS</span></span>
<span data-ttu-id="88e92-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl вернет URL-адрес контейнерной непрерывной развертки</span><span class="sxs-lookup"><span data-stu-id="88e92-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88e92-104">SYNTAX</span></span>

### <span data-ttu-id="88e92-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="88e92-105">S1</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88e92-106">S2</span><span class="sxs-lookup"><span data-stu-id="88e92-106">S2</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88e92-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88e92-107">DESCRIPTION</span></span>
<span data-ttu-id="88e92-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl вернет URL-адрес контейнерной непрерывной развертки</span><span class="sxs-lookup"><span data-stu-id="88e92-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="88e92-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88e92-109">EXAMPLES</span></span>

### <span data-ttu-id="88e92-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88e92-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="88e92-111">Эта команда вернет URL-адрес непрерывного развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="88e92-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="88e92-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88e92-112">PARAMETERS</span></span>

### <span data-ttu-id="88e92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e92-113">-DefaultProfile</span></span>
<span data-ttu-id="88e92-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88e92-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e92-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88e92-115">-Name</span></span>
<span data-ttu-id="88e92-116">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="88e92-116">The name of the web app.</span></span>

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

### <span data-ttu-id="88e92-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e92-117">-ResourceGroupName</span></span>
<span data-ttu-id="88e92-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88e92-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="88e92-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="88e92-119">-SlotName</span></span>
<span data-ttu-id="88e92-120">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="88e92-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="88e92-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="88e92-121">-WebApp</span></span>
<span data-ttu-id="88e92-122">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="88e92-122">The web app object</span></span>

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

### <span data-ttu-id="88e92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e92-123">CommonParameters</span></span>
<span data-ttu-id="88e92-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88e92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e92-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e92-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e92-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88e92-126">INPUTS</span></span>

### <span data-ttu-id="88e92-127">System. String</span><span class="sxs-lookup"><span data-stu-id="88e92-127">System.String</span></span>
### <span data-ttu-id="88e92-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="88e92-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="88e92-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88e92-129">OUTPUTS</span></span>

### <span data-ttu-id="88e92-130">System. String</span><span class="sxs-lookup"><span data-stu-id="88e92-130">System.String</span></span>
## <span data-ttu-id="88e92-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="88e92-131">NOTES</span></span>

## <span data-ttu-id="88e92-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88e92-132">RELATED LINKS</span></span>
