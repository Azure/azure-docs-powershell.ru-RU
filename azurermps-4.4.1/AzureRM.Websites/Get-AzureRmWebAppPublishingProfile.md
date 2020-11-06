---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a05dfcbf509ccb68c0b928467a5695361a4916e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561972"
---
# <span data-ttu-id="e5703-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e5703-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="e5703-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5703-102">SYNOPSIS</span></span>
<span data-ttu-id="e5703-103">Получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e5703-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5703-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5703-104">SYNTAX</span></span>

### <span data-ttu-id="e5703-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="e5703-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5703-106">S2</span><span class="sxs-lookup"><span data-stu-id="e5703-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5703-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5703-107">DESCRIPTION</span></span>
<span data-ttu-id="e5703-108">Командлет **Get-AzureRmWebAppPublishingProfile** получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e5703-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="e5703-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5703-109">EXAMPLES</span></span>

### <span data-ttu-id="e5703-110">1:</span><span class="sxs-lookup"><span data-stu-id="e5703-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="e5703-111">Эта команда получает профиль публикации в формате FTP для веб-приложения ContosoWebApp, связанного с группой ресурсов Default-Web-WestUS, и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="e5703-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="e5703-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5703-112">PARAMETERS</span></span>

### <span data-ttu-id="e5703-113">-Format</span><span class="sxs-lookup"><span data-stu-id="e5703-113">-Format</span></span>
<span data-ttu-id="e5703-114">Формате</span><span class="sxs-lookup"><span data-stu-id="e5703-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5703-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5703-115">-Name</span></span>
<span data-ttu-id="e5703-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="e5703-116">WebApp Name</span></span>

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

### <span data-ttu-id="e5703-117">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="e5703-117">-OutputFile</span></span>
<span data-ttu-id="e5703-118">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="e5703-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5703-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5703-119">-ResourceGroupName</span></span>
<span data-ttu-id="e5703-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e5703-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e5703-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e5703-121">-WebApp</span></span>
<span data-ttu-id="e5703-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="e5703-122">WebApp Object</span></span>

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

### <span data-ttu-id="e5703-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5703-123">-DefaultProfile</span></span>
<span data-ttu-id="e5703-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5703-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5703-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5703-125">CommonParameters</span></span>
<span data-ttu-id="e5703-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5703-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5703-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5703-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5703-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5703-128">INPUTS</span></span>

### <span data-ttu-id="e5703-129">Семейств</span><span class="sxs-lookup"><span data-stu-id="e5703-129">Site</span></span>
<span data-ttu-id="e5703-130">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e5703-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e5703-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5703-131">OUTPUTS</span></span>

## <span data-ttu-id="e5703-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5703-132">NOTES</span></span>

## <span data-ttu-id="e5703-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5703-133">RELATED LINKS</span></span>

[<span data-ttu-id="e5703-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5703-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="e5703-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e5703-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


