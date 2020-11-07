---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910548"
---
# <span data-ttu-id="eb8ee-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="eb8ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8ee-103">Останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8ee-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="eb8ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb8ee-104">SYNTAX</span></span>

### <span data-ttu-id="eb8ee-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="eb8ee-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb8ee-106">S2</span><span class="sxs-lookup"><span data-stu-id="eb8ee-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb8ee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb8ee-107">DESCRIPTION</span></span>
<span data-ttu-id="eb8ee-108">Командлет **Stop-AzWebApp** останавливает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8ee-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="eb8ee-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb8ee-109">EXAMPLES</span></span>

### <span data-ttu-id="eb8ee-110">Пример 1: остановка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="eb8ee-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="eb8ee-111">Эта команда останавливает веб-приложение ContosoWebApp, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="eb8ee-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="eb8ee-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb8ee-112">PARAMETERS</span></span>

### <span data-ttu-id="eb8ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8ee-113">-DefaultProfile</span></span>
<span data-ttu-id="eb8ee-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb8ee-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb8ee-115">-Name</span></span>
<span data-ttu-id="eb8ee-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-116">WebApp Name</span></span>

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

### <span data-ttu-id="eb8ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb8ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb8ee-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eb8ee-118">Resource Group Name</span></span>

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

### <span data-ttu-id="eb8ee-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-119">-WebApp</span></span>
<span data-ttu-id="eb8ee-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-120">WebApp Object</span></span>

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

### <span data-ttu-id="eb8ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8ee-121">CommonParameters</span></span>
<span data-ttu-id="eb8ee-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb8ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8ee-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8ee-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8ee-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb8ee-124">INPUTS</span></span>

### <span data-ttu-id="eb8ee-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="eb8ee-125">Site</span></span>
<span data-ttu-id="eb8ee-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eb8ee-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eb8ee-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb8ee-127">OUTPUTS</span></span>

## <span data-ttu-id="eb8ee-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb8ee-128">NOTES</span></span>

## <span data-ttu-id="eb8ee-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb8ee-129">RELATED LINKS</span></span>

[<span data-ttu-id="eb8ee-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="eb8ee-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="eb8ee-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="eb8ee-133">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="eb8ee-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eb8ee-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


