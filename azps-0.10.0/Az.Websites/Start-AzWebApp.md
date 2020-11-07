---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: d533a2d7401236e374ca6f541e646cb85a080f9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910562"
---
# <span data-ttu-id="cfece-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-101">Start-AzWebApp</span></span>

## <span data-ttu-id="cfece-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfece-102">SYNOPSIS</span></span>
<span data-ttu-id="cfece-103">Запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="cfece-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="cfece-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfece-104">SYNTAX</span></span>

### <span data-ttu-id="cfece-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="cfece-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfece-106">S2</span><span class="sxs-lookup"><span data-stu-id="cfece-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfece-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfece-107">DESCRIPTION</span></span>
<span data-ttu-id="cfece-108">Командлет **Start-AzWebApp** запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="cfece-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="cfece-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfece-109">EXAMPLES</span></span>

### <span data-ttu-id="cfece-110">Пример 1: запуск веб-приложения</span><span class="sxs-lookup"><span data-stu-id="cfece-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="cfece-111">Эта команда запускает веб-приложение с именем ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="cfece-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="cfece-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfece-112">PARAMETERS</span></span>

### <span data-ttu-id="cfece-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfece-113">-DefaultProfile</span></span>
<span data-ttu-id="cfece-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfece-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfece-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cfece-115">-Name</span></span>
<span data-ttu-id="cfece-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-116">WebApp Name</span></span>

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

### <span data-ttu-id="cfece-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfece-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfece-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cfece-118">Resource Group Name</span></span>

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

### <span data-ttu-id="cfece-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-119">-WebApp</span></span>
<span data-ttu-id="cfece-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-120">WebApp Object</span></span>

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

### <span data-ttu-id="cfece-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfece-121">CommonParameters</span></span>
<span data-ttu-id="cfece-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfece-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfece-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfece-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfece-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfece-124">INPUTS</span></span>

### <span data-ttu-id="cfece-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="cfece-125">Site</span></span>
<span data-ttu-id="cfece-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cfece-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cfece-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfece-127">OUTPUTS</span></span>

## <span data-ttu-id="cfece-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfece-128">NOTES</span></span>

## <span data-ttu-id="cfece-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfece-129">RELATED LINKS</span></span>

[<span data-ttu-id="cfece-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="cfece-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="cfece-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="cfece-133">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="cfece-134">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cfece-134">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


