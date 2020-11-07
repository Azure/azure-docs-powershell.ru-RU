---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: cedaf16333d69a25dce0ce2657640e723767aece
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910605"
---
# <span data-ttu-id="56e73-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="56e73-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="56e73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56e73-102">SYNOPSIS</span></span>
<span data-ttu-id="56e73-103">Получает профиль публикации слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="56e73-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="56e73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56e73-104">SYNTAX</span></span>

### <span data-ttu-id="56e73-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="56e73-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56e73-106">S2</span><span class="sxs-lookup"><span data-stu-id="56e73-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e73-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56e73-107">DESCRIPTION</span></span>
<span data-ttu-id="56e73-108">Командлет **Get-AzWebAppSlotPublishingProfile** получает профиль публикации веб-приложения для заданной области.</span><span class="sxs-lookup"><span data-stu-id="56e73-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="56e73-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56e73-109">EXAMPLES</span></span>

### <span data-ttu-id="56e73-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56e73-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="56e73-111">Эта команда получает профиль публикации в формате FTP для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-Web-WestUS и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="56e73-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="56e73-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56e73-112">PARAMETERS</span></span>

### <span data-ttu-id="56e73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e73-113">-DefaultProfile</span></span>
<span data-ttu-id="56e73-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56e73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e73-115">-Format</span><span class="sxs-lookup"><span data-stu-id="56e73-115">-Format</span></span>
<span data-ttu-id="56e73-116">Формате</span><span class="sxs-lookup"><span data-stu-id="56e73-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e73-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56e73-117">-Name</span></span>
<span data-ttu-id="56e73-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="56e73-118">WebApp Name</span></span>

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

### <span data-ttu-id="56e73-119">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="56e73-119">-OutputFile</span></span>
<span data-ttu-id="56e73-120">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="56e73-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e73-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e73-121">-ResourceGroupName</span></span>
<span data-ttu-id="56e73-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="56e73-122">Resource Group Name</span></span>

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

### <span data-ttu-id="56e73-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="56e73-123">-Slot</span></span>
<span data-ttu-id="56e73-124">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="56e73-124">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e73-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="56e73-125">-WebApp</span></span>
<span data-ttu-id="56e73-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="56e73-126">WebApp Object</span></span>

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

### <span data-ttu-id="56e73-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e73-127">CommonParameters</span></span>
<span data-ttu-id="56e73-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56e73-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e73-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e73-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e73-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56e73-130">INPUTS</span></span>

### <span data-ttu-id="56e73-131">Семейств</span><span class="sxs-lookup"><span data-stu-id="56e73-131">Site</span></span>
<span data-ttu-id="56e73-132">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="56e73-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="56e73-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56e73-133">OUTPUTS</span></span>

## <span data-ttu-id="56e73-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="56e73-134">NOTES</span></span>

## <span data-ttu-id="56e73-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56e73-135">RELATED LINKS</span></span>

[<span data-ttu-id="56e73-136">Сброс — AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="56e73-136">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="56e73-137">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56e73-137">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="56e73-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="56e73-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
