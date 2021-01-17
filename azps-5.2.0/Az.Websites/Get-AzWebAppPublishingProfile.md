---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323109"
---
# <span data-ttu-id="c5020-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c5020-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="c5020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5020-102">SYNOPSIS</span></span>
<span data-ttu-id="c5020-103">Получает профиль публикации Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c5020-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="c5020-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5020-104">SYNTAX</span></span>

### <span data-ttu-id="c5020-105">S1</span><span class="sxs-lookup"><span data-stu-id="c5020-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5020-106">S2</span><span class="sxs-lookup"><span data-stu-id="c5020-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5020-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5020-107">DESCRIPTION</span></span>
<span data-ttu-id="c5020-108">Для получения профиля публикации Azure Web App возвращается **cmdlet Get-AzWebAppPublishingProfile.**</span><span class="sxs-lookup"><span data-stu-id="c5020-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="c5020-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5020-109">EXAMPLES</span></span>

### <span data-ttu-id="c5020-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c5020-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="c5020-111">Эта команда получает профиль публикации в формате Ftp для Web App ContosoWebApp, связанный с группой ресурсов Default-Web-WestUS, и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="c5020-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="c5020-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5020-112">PARAMETERS</span></span>

### <span data-ttu-id="c5020-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5020-113">-DefaultProfile</span></span>
<span data-ttu-id="c5020-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5020-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5020-115">-Format</span><span class="sxs-lookup"><span data-stu-id="c5020-115">-Format</span></span>
<span data-ttu-id="c5020-116">Формат</span><span class="sxs-lookup"><span data-stu-id="c5020-116">Format</span></span>

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

### <span data-ttu-id="c5020-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="c5020-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="c5020-118">Включить конечные точки аварийного восстановления, если это так</span><span class="sxs-lookup"><span data-stu-id="c5020-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="c5020-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c5020-119">-Name</span></span>
<span data-ttu-id="c5020-120">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c5020-120">WebApp Name</span></span>

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

### <span data-ttu-id="c5020-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="c5020-121">-OutputFile</span></span>
<span data-ttu-id="c5020-122">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="c5020-122">Output File</span></span>

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

### <span data-ttu-id="c5020-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5020-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5020-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c5020-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c5020-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c5020-125">-WebApp</span></span>
<span data-ttu-id="c5020-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="c5020-126">WebApp Object</span></span>

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

### <span data-ttu-id="c5020-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5020-127">CommonParameters</span></span>
<span data-ttu-id="c5020-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5020-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5020-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5020-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5020-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5020-130">INPUTS</span></span>

### <span data-ttu-id="c5020-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c5020-131">System.String</span></span>

### <span data-ttu-id="c5020-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c5020-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c5020-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5020-133">OUTPUTS</span></span>

### <span data-ttu-id="c5020-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c5020-134">System.String</span></span>

## <span data-ttu-id="c5020-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5020-135">NOTES</span></span>

## <span data-ttu-id="c5020-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5020-136">RELATED LINKS</span></span>

[<span data-ttu-id="c5020-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c5020-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="c5020-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c5020-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


