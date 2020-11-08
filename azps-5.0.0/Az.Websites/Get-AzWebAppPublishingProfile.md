---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249421"
---
# <span data-ttu-id="1dfca-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1dfca-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="1dfca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1dfca-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfca-103">Получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfca-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="1dfca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1dfca-104">SYNTAX</span></span>

### <span data-ttu-id="1dfca-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="1dfca-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dfca-106">S2</span><span class="sxs-lookup"><span data-stu-id="1dfca-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dfca-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dfca-107">DESCRIPTION</span></span>
<span data-ttu-id="1dfca-108">Командлет **Get-AzWebAppPublishingProfile** получает профиль публикации веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfca-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="1dfca-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1dfca-109">EXAMPLES</span></span>

### <span data-ttu-id="1dfca-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1dfca-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="1dfca-111">Эта команда получает профиль публикации в формате FTP для веб-приложения ContosoWebApp, связанного с группой ресурсов Default-Web-WestUS, и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="1dfca-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="1dfca-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1dfca-112">PARAMETERS</span></span>

### <span data-ttu-id="1dfca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dfca-113">-DefaultProfile</span></span>
<span data-ttu-id="1dfca-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dfca-115">-Format</span><span class="sxs-lookup"><span data-stu-id="1dfca-115">-Format</span></span>
<span data-ttu-id="1dfca-116">Формате</span><span class="sxs-lookup"><span data-stu-id="1dfca-116">Format</span></span>

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

### <span data-ttu-id="1dfca-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="1dfca-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="1dfca-118">Включать конечные точки восстановления после сбоя (истина)</span><span class="sxs-lookup"><span data-stu-id="1dfca-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dfca-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1dfca-119">-Name</span></span>
<span data-ttu-id="1dfca-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="1dfca-120">WebApp Name</span></span>

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

### <span data-ttu-id="1dfca-121">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="1dfca-121">-OutputFile</span></span>
<span data-ttu-id="1dfca-122">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="1dfca-122">Output File</span></span>

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

### <span data-ttu-id="1dfca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dfca-123">-ResourceGroupName</span></span>
<span data-ttu-id="1dfca-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1dfca-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1dfca-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1dfca-125">-WebApp</span></span>
<span data-ttu-id="1dfca-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="1dfca-126">WebApp Object</span></span>

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

### <span data-ttu-id="1dfca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfca-127">CommonParameters</span></span>
<span data-ttu-id="1dfca-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1dfca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfca-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dfca-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfca-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1dfca-130">INPUTS</span></span>

### <span data-ttu-id="1dfca-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1dfca-131">System.String</span></span>

### <span data-ttu-id="1dfca-132">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="1dfca-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1dfca-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dfca-133">OUTPUTS</span></span>

### <span data-ttu-id="1dfca-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1dfca-134">System.String</span></span>

## <span data-ttu-id="1dfca-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="1dfca-135">NOTES</span></span>

## <span data-ttu-id="1dfca-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1dfca-136">RELATED LINKS</span></span>

[<span data-ttu-id="1dfca-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1dfca-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="1dfca-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1dfca-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


