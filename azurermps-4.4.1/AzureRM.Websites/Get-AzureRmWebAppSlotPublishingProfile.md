---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: d8ccd8f1011a73068c24323bb86e39340dfc9573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563808"
---
# <span data-ttu-id="b241a-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b241a-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="b241a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b241a-102">SYNOPSIS</span></span>
<span data-ttu-id="b241a-103">Получает профиль публикации слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b241a-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b241a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b241a-104">SYNTAX</span></span>

### <span data-ttu-id="b241a-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="b241a-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b241a-106">S2</span><span class="sxs-lookup"><span data-stu-id="b241a-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b241a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b241a-107">DESCRIPTION</span></span>
<span data-ttu-id="b241a-108">Командлет **Get-AzureRmWebAppSlotPublishingProfile** получает профиль публикации веб-приложения для заданной области.</span><span class="sxs-lookup"><span data-stu-id="b241a-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="b241a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b241a-109">EXAMPLES</span></span>

### <span data-ttu-id="b241a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b241a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="b241a-111">Эта команда получает профиль публикации в формате FTP для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-Web-WestUS и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="b241a-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="b241a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b241a-112">PARAMETERS</span></span>

### <span data-ttu-id="b241a-113">-Format</span><span class="sxs-lookup"><span data-stu-id="b241a-113">-Format</span></span>
<span data-ttu-id="b241a-114">Формате</span><span class="sxs-lookup"><span data-stu-id="b241a-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b241a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b241a-115">-Name</span></span>
<span data-ttu-id="b241a-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="b241a-116">WebApp Name</span></span>

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

### <span data-ttu-id="b241a-117">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="b241a-117">-OutputFile</span></span>
<span data-ttu-id="b241a-118">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="b241a-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b241a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b241a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b241a-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b241a-120">Resource Group Name</span></span>

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

### <span data-ttu-id="b241a-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="b241a-121">-Slot</span></span>
<span data-ttu-id="b241a-122">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="b241a-122">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b241a-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b241a-123">-WebApp</span></span>
<span data-ttu-id="b241a-124">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="b241a-124">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b241a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b241a-125">-DefaultProfile</span></span>
<span data-ttu-id="b241a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b241a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b241a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b241a-127">CommonParameters</span></span>
<span data-ttu-id="b241a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b241a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b241a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b241a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b241a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b241a-130">INPUTS</span></span>

### <span data-ttu-id="b241a-131">Семейств</span><span class="sxs-lookup"><span data-stu-id="b241a-131">Site</span></span>
<span data-ttu-id="b241a-132">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b241a-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b241a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b241a-133">OUTPUTS</span></span>

## <span data-ttu-id="b241a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b241a-134">NOTES</span></span>

## <span data-ttu-id="b241a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b241a-135">RELATED LINKS</span></span>

[<span data-ttu-id="b241a-136">Сброс — AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b241a-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="b241a-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b241a-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="b241a-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b241a-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
