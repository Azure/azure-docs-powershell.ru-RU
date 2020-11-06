---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 1202d15504717052513f1ef77a21e008fefe20af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558712"
---
# <span data-ttu-id="62c4a-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="62c4a-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="62c4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="62c4a-103">Получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="62c4a-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62c4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62c4a-104">SYNTAX</span></span>

### <span data-ttu-id="62c4a-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="62c4a-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62c4a-106">S2</span><span class="sxs-lookup"><span data-stu-id="62c4a-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62c4a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="62c4a-108">Командлет **Get-AzureRmWebAppPublishingProfile** получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="62c4a-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="62c4a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62c4a-109">EXAMPLES</span></span>

### <span data-ttu-id="62c4a-110">1:</span><span class="sxs-lookup"><span data-stu-id="62c4a-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="62c4a-111">Эта команда получает профиль публикации в формате FTP для веб-приложения ContosoWebApp, связанного с группой ресурсов Default-Web-WestUS, и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="62c4a-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="62c4a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62c4a-112">PARAMETERS</span></span>

### <span data-ttu-id="62c4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c4a-113">-DefaultProfile</span></span>
<span data-ttu-id="62c4a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62c4a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c4a-115">-Format</span><span class="sxs-lookup"><span data-stu-id="62c4a-115">-Format</span></span>
<span data-ttu-id="62c4a-116">Формате</span><span class="sxs-lookup"><span data-stu-id="62c4a-116">Format</span></span>

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

### <span data-ttu-id="62c4a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62c4a-117">-Name</span></span>
<span data-ttu-id="62c4a-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="62c4a-118">WebApp Name</span></span>

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

### <span data-ttu-id="62c4a-119">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="62c4a-119">-OutputFile</span></span>
<span data-ttu-id="62c4a-120">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="62c4a-120">Output File</span></span>

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

### <span data-ttu-id="62c4a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c4a-121">-ResourceGroupName</span></span>
<span data-ttu-id="62c4a-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="62c4a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="62c4a-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="62c4a-123">-WebApp</span></span>
<span data-ttu-id="62c4a-124">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="62c4a-124">WebApp Object</span></span>

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

### <span data-ttu-id="62c4a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c4a-125">CommonParameters</span></span>
<span data-ttu-id="62c4a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62c4a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c4a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c4a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c4a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62c4a-128">INPUTS</span></span>

### <span data-ttu-id="62c4a-129">Семейств</span><span class="sxs-lookup"><span data-stu-id="62c4a-129">Site</span></span>
<span data-ttu-id="62c4a-130">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="62c4a-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="62c4a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62c4a-131">OUTPUTS</span></span>

## <span data-ttu-id="62c4a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="62c4a-132">NOTES</span></span>

## <span data-ttu-id="62c4a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62c4a-133">RELATED LINKS</span></span>

[<span data-ttu-id="62c4a-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="62c4a-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="62c4a-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="62c4a-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


