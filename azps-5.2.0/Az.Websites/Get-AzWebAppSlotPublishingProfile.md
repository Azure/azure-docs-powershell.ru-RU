---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399236"
---
# <span data-ttu-id="505a5-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="505a5-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="505a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="505a5-102">SYNOPSIS</span></span>
<span data-ttu-id="505a5-103">Получает профиль публикации слота Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="505a5-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="505a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="505a5-104">SYNTAX</span></span>

### <span data-ttu-id="505a5-105">S1</span><span class="sxs-lookup"><span data-stu-id="505a5-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="505a5-106">S2</span><span class="sxs-lookup"><span data-stu-id="505a5-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="505a5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="505a5-107">DESCRIPTION</span></span>
<span data-ttu-id="505a5-108">Для указанного слота профиль публикации Web App возвращается с помощью cmdlet **Get-AzWebAppSlotPublishingProfile.**</span><span class="sxs-lookup"><span data-stu-id="505a5-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="505a5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="505a5-109">EXAMPLES</span></span>

### <span data-ttu-id="505a5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="505a5-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="505a5-111">Эта команда получает профиль публикации в формате Ftp для slot Slot001, связанный с web App ContosoWebApp, связанный с группой ресурсов Default-Web-WestUS, и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="505a5-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="505a5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="505a5-112">PARAMETERS</span></span>

### <span data-ttu-id="505a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505a5-113">-DefaultProfile</span></span>
<span data-ttu-id="505a5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="505a5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="505a5-115">-Format</span><span class="sxs-lookup"><span data-stu-id="505a5-115">-Format</span></span>
<span data-ttu-id="505a5-116">Формат</span><span class="sxs-lookup"><span data-stu-id="505a5-116">Format</span></span>

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

### <span data-ttu-id="505a5-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="505a5-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="505a5-118">Включить конечные точки аварийного восстановления, если это так</span><span class="sxs-lookup"><span data-stu-id="505a5-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="505a5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="505a5-119">-Name</span></span>
<span data-ttu-id="505a5-120">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="505a5-120">WebApp Name</span></span>

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

### <span data-ttu-id="505a5-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="505a5-121">-OutputFile</span></span>
<span data-ttu-id="505a5-122">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="505a5-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505a5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="505a5-123">-ResourceGroupName</span></span>
<span data-ttu-id="505a5-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="505a5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="505a5-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="505a5-125">-Slot</span></span>
<span data-ttu-id="505a5-126">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="505a5-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="505a5-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="505a5-127">-WebApp</span></span>
<span data-ttu-id="505a5-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="505a5-128">WebApp Object</span></span>

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

### <span data-ttu-id="505a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505a5-129">CommonParameters</span></span>
<span data-ttu-id="505a5-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="505a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505a5-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="505a5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505a5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="505a5-132">INPUTS</span></span>

### <span data-ttu-id="505a5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="505a5-133">System.String</span></span>

### <span data-ttu-id="505a5-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="505a5-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="505a5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="505a5-135">OUTPUTS</span></span>

### <span data-ttu-id="505a5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="505a5-136">System.String</span></span>

## <span data-ttu-id="505a5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="505a5-137">NOTES</span></span>

## <span data-ttu-id="505a5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="505a5-138">RELATED LINKS</span></span>

[<span data-ttu-id="505a5-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="505a5-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="505a5-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="505a5-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="505a5-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="505a5-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
