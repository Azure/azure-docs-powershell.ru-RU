---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: d1e4e029676eadec3f793aff99a2d68983891f2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567854"
---
# <span data-ttu-id="146ba-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="146ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="146ba-102">SYNOPSIS</span></span>
<span data-ttu-id="146ba-103">Останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="146ba-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="146ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="146ba-104">SYNTAX</span></span>

### <span data-ttu-id="146ba-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="146ba-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="146ba-106">S2</span><span class="sxs-lookup"><span data-stu-id="146ba-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="146ba-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="146ba-107">DESCRIPTION</span></span>
<span data-ttu-id="146ba-108">Командлет **Stop-AzureRmWebApp** останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="146ba-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="146ba-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="146ba-109">EXAMPLES</span></span>

### <span data-ttu-id="146ba-110">Пример 1: остановка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="146ba-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="146ba-111">Эта команда останавливает веб-приложение ContosoWebApp, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="146ba-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="146ba-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="146ba-112">PARAMETERS</span></span>

### <span data-ttu-id="146ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="146ba-113">-DefaultProfile</span></span>
<span data-ttu-id="146ba-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="146ba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="146ba-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="146ba-115">-Name</span></span>
<span data-ttu-id="146ba-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="146ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="146ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="146ba-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="146ba-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="146ba-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-119">-WebApp</span></span>
<span data-ttu-id="146ba-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="146ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146ba-121">CommonParameters</span></span>
<span data-ttu-id="146ba-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="146ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146ba-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="146ba-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146ba-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="146ba-124">INPUTS</span></span>

### <span data-ttu-id="146ba-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="146ba-125">Site</span></span>
<span data-ttu-id="146ba-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="146ba-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="146ba-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="146ba-127">OUTPUTS</span></span>

## <span data-ttu-id="146ba-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="146ba-128">NOTES</span></span>

## <span data-ttu-id="146ba-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="146ba-129">RELATED LINKS</span></span>

[<span data-ttu-id="146ba-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="146ba-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="146ba-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="146ba-133">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="146ba-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="146ba-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


