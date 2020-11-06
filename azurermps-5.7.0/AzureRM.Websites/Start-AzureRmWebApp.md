---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 74f0fcfdcbbc71781debef62becb36018ecb51a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557019"
---
# <span data-ttu-id="91922-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91922-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="91922-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91922-102">SYNOPSIS</span></span>
<span data-ttu-id="91922-103">Запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="91922-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91922-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91922-104">SYNTAX</span></span>

### <span data-ttu-id="91922-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="91922-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91922-106">S2</span><span class="sxs-lookup"><span data-stu-id="91922-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91922-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91922-107">DESCRIPTION</span></span>
<span data-ttu-id="91922-108">Командлет **Start-AzureRmWebApp** запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="91922-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="91922-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91922-109">EXAMPLES</span></span>

### <span data-ttu-id="91922-110">Пример 1: запуск веб-приложения</span><span class="sxs-lookup"><span data-stu-id="91922-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="91922-111">Эта команда запускает веб-приложение с именем ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="91922-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="91922-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91922-112">PARAMETERS</span></span>

### <span data-ttu-id="91922-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91922-113">-DefaultProfile</span></span>
<span data-ttu-id="91922-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91922-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91922-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91922-115">-Name</span></span>
<span data-ttu-id="91922-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="91922-116">WebApp Name</span></span>

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

### <span data-ttu-id="91922-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91922-117">-ResourceGroupName</span></span>
<span data-ttu-id="91922-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="91922-118">Resource Group Name</span></span>

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

### <span data-ttu-id="91922-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="91922-119">-WebApp</span></span>
<span data-ttu-id="91922-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="91922-120">WebApp Object</span></span>

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

### <span data-ttu-id="91922-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91922-121">CommonParameters</span></span>
<span data-ttu-id="91922-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91922-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91922-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91922-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91922-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91922-124">INPUTS</span></span>

### <span data-ttu-id="91922-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="91922-125">Site</span></span>
<span data-ttu-id="91922-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="91922-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="91922-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91922-127">OUTPUTS</span></span>

## <span data-ttu-id="91922-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="91922-128">NOTES</span></span>

## <span data-ttu-id="91922-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91922-129">RELATED LINKS</span></span>

[<span data-ttu-id="91922-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91922-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="91922-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91922-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="91922-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91922-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="91922-133">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91922-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="91922-134">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91922-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


