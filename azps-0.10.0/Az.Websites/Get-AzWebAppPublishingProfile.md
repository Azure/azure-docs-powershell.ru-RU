---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 477b60400082954eb12bd0756fb4380ece2a35ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910610"
---
# <span data-ttu-id="290e1-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="290e1-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="290e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="290e1-102">SYNOPSIS</span></span>
<span data-ttu-id="290e1-103">Получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="290e1-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="290e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="290e1-104">SYNTAX</span></span>

### <span data-ttu-id="290e1-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="290e1-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="290e1-106">S2</span><span class="sxs-lookup"><span data-stu-id="290e1-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="290e1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="290e1-107">DESCRIPTION</span></span>
<span data-ttu-id="290e1-108">Командлет **Get-AzWebAppPublishingProfile** получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="290e1-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="290e1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="290e1-109">EXAMPLES</span></span>

### <span data-ttu-id="290e1-110">1:</span><span class="sxs-lookup"><span data-stu-id="290e1-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="290e1-111">Эта команда получает профиль публикации в формате FTP для веб-приложения ContosoWebApp, связанного с группой ресурсов Default-Web-WestUS, и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="290e1-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="290e1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="290e1-112">PARAMETERS</span></span>

### <span data-ttu-id="290e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="290e1-113">-DefaultProfile</span></span>
<span data-ttu-id="290e1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="290e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="290e1-115">-Format</span><span class="sxs-lookup"><span data-stu-id="290e1-115">-Format</span></span>
<span data-ttu-id="290e1-116">Формате</span><span class="sxs-lookup"><span data-stu-id="290e1-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="290e1-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="290e1-117">-Name</span></span>
<span data-ttu-id="290e1-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="290e1-118">WebApp Name</span></span>

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

### <span data-ttu-id="290e1-119">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="290e1-119">-OutputFile</span></span>
<span data-ttu-id="290e1-120">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="290e1-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="290e1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="290e1-121">-ResourceGroupName</span></span>
<span data-ttu-id="290e1-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="290e1-122">Resource Group Name</span></span>

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

### <span data-ttu-id="290e1-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="290e1-123">-WebApp</span></span>
<span data-ttu-id="290e1-124">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="290e1-124">WebApp Object</span></span>

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

### <span data-ttu-id="290e1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="290e1-125">CommonParameters</span></span>
<span data-ttu-id="290e1-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="290e1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="290e1-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="290e1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="290e1-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="290e1-128">INPUTS</span></span>

### <span data-ttu-id="290e1-129">Семейств</span><span class="sxs-lookup"><span data-stu-id="290e1-129">Site</span></span>
<span data-ttu-id="290e1-130">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="290e1-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="290e1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="290e1-131">OUTPUTS</span></span>

## <span data-ttu-id="290e1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="290e1-132">NOTES</span></span>

## <span data-ttu-id="290e1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="290e1-133">RELATED LINKS</span></span>

[<span data-ttu-id="290e1-134">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="290e1-134">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="290e1-135">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="290e1-135">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


