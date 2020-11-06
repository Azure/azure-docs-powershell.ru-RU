---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562492"
---
# <span data-ttu-id="88acd-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="88acd-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="88acd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88acd-102">SYNOPSIS</span></span>
<span data-ttu-id="88acd-103">Получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="88acd-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88acd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88acd-104">SYNTAX</span></span>

### <span data-ttu-id="88acd-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="88acd-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88acd-106">S2</span><span class="sxs-lookup"><span data-stu-id="88acd-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88acd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88acd-107">DESCRIPTION</span></span>
<span data-ttu-id="88acd-108">Командлет **Get-AzureRmWebAppPublishingProfile** получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="88acd-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="88acd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88acd-109">EXAMPLES</span></span>

### <span data-ttu-id="88acd-110">1:</span><span class="sxs-lookup"><span data-stu-id="88acd-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="88acd-111">Эта команда получает профиль публикации в формате FTP для веб-приложения ContosoWebApp, связанного с группой ресурсов Default-Web-WestUS, и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="88acd-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="88acd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88acd-112">PARAMETERS</span></span>

### <span data-ttu-id="88acd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88acd-113">-DefaultProfile</span></span>
<span data-ttu-id="88acd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88acd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88acd-115">-Format</span><span class="sxs-lookup"><span data-stu-id="88acd-115">-Format</span></span>
<span data-ttu-id="88acd-116">Формате</span><span class="sxs-lookup"><span data-stu-id="88acd-116">Format</span></span>

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

### <span data-ttu-id="88acd-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="88acd-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="88acd-118">Включать конечные точки восстановления после сбоя (истина)</span><span class="sxs-lookup"><span data-stu-id="88acd-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88acd-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88acd-119">-Name</span></span>
<span data-ttu-id="88acd-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="88acd-120">WebApp Name</span></span>

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

### <span data-ttu-id="88acd-121">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="88acd-121">-OutputFile</span></span>
<span data-ttu-id="88acd-122">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="88acd-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88acd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88acd-123">-ResourceGroupName</span></span>
<span data-ttu-id="88acd-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="88acd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="88acd-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="88acd-125">-WebApp</span></span>
<span data-ttu-id="88acd-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="88acd-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88acd-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="88acd-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="88acd-128">Включать конечные точки восстановления после сбоя (истина)</span><span class="sxs-lookup"><span data-stu-id="88acd-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88acd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88acd-129">CommonParameters</span></span>
<span data-ttu-id="88acd-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88acd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88acd-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88acd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88acd-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88acd-132">INPUTS</span></span>

### <span data-ttu-id="88acd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="88acd-133">System.String</span></span>

### <span data-ttu-id="88acd-134">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="88acd-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="88acd-135">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="88acd-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="88acd-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88acd-136">OUTPUTS</span></span>

### <span data-ttu-id="88acd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="88acd-137">System.String</span></span>

## <span data-ttu-id="88acd-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="88acd-138">NOTES</span></span>

## <span data-ttu-id="88acd-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88acd-139">RELATED LINKS</span></span>

[<span data-ttu-id="88acd-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="88acd-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="88acd-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="88acd-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


