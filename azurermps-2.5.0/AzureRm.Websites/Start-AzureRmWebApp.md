---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: b05ba189c4b718689f95acac1bfcead84cd3415b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914329"
---
# <span data-ttu-id="eab8b-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="eab8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eab8b-102">SYNOPSIS</span></span>
<span data-ttu-id="eab8b-103">Запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="eab8b-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eab8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eab8b-104">SYNTAX</span></span>

### <span data-ttu-id="eab8b-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="eab8b-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eab8b-106">S2</span><span class="sxs-lookup"><span data-stu-id="eab8b-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eab8b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eab8b-107">DESCRIPTION</span></span>
<span data-ttu-id="eab8b-108">Командлет **Start-AzureRmWebApp** запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="eab8b-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="eab8b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eab8b-109">EXAMPLES</span></span>

### <span data-ttu-id="eab8b-110">Пример 1: запуск веб-приложения</span><span class="sxs-lookup"><span data-stu-id="eab8b-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="eab8b-111">Эта команда запускает веб-приложение с именем ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="eab8b-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="eab8b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eab8b-112">PARAMETERS</span></span>

### <span data-ttu-id="eab8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab8b-113">-DefaultProfile</span></span>
<span data-ttu-id="eab8b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eab8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eab8b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eab8b-115">-Name</span></span>
<span data-ttu-id="eab8b-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-116">WebApp Name</span></span>

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

### <span data-ttu-id="eab8b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eab8b-117">-ResourceGroupName</span></span>
<span data-ttu-id="eab8b-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eab8b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="eab8b-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-119">-WebApp</span></span>
<span data-ttu-id="eab8b-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-120">WebApp Object</span></span>

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

### <span data-ttu-id="eab8b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab8b-121">CommonParameters</span></span>
<span data-ttu-id="eab8b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eab8b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab8b-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eab8b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab8b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eab8b-124">INPUTS</span></span>

### <span data-ttu-id="eab8b-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="eab8b-125">Site</span></span>
<span data-ttu-id="eab8b-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eab8b-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eab8b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eab8b-127">OUTPUTS</span></span>

## <span data-ttu-id="eab8b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="eab8b-128">NOTES</span></span>

## <span data-ttu-id="eab8b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eab8b-129">RELATED LINKS</span></span>

[<span data-ttu-id="eab8b-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="eab8b-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="eab8b-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="eab8b-133">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="eab8b-134">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eab8b-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


