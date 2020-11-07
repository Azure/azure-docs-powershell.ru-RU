---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 615fcc228be9ef0e3e0d23c6463859c20ff7da11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728344"
---
# <span data-ttu-id="349d3-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="349d3-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="349d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="349d3-102">SYNOPSIS</span></span>
<span data-ttu-id="349d3-103">Получает профиль публикации слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="349d3-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="349d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="349d3-104">SYNTAX</span></span>

### <span data-ttu-id="349d3-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="349d3-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-106">S2</span><span class="sxs-lookup"><span data-stu-id="349d3-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="349d3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="349d3-107">DESCRIPTION</span></span>
<span data-ttu-id="349d3-108">Командлет **Get-AzWebAppSlotPublishingProfile** получает профиль публикации веб-приложения для заданной области.</span><span class="sxs-lookup"><span data-stu-id="349d3-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="349d3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="349d3-109">EXAMPLES</span></span>

### <span data-ttu-id="349d3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="349d3-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="349d3-111">Эта команда получает профиль публикации в формате FTP для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-Web-WestUS и сохраняет его в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="349d3-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="349d3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="349d3-112">PARAMETERS</span></span>

### <span data-ttu-id="349d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349d3-113">-DefaultProfile</span></span>
<span data-ttu-id="349d3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="349d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="349d3-115">-Format</span><span class="sxs-lookup"><span data-stu-id="349d3-115">-Format</span></span>
<span data-ttu-id="349d3-116">Формате</span><span class="sxs-lookup"><span data-stu-id="349d3-116">Format</span></span>

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

### <span data-ttu-id="349d3-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="349d3-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="349d3-118">Включать конечные точки восстановления после сбоя (истина)</span><span class="sxs-lookup"><span data-stu-id="349d3-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="349d3-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="349d3-119">-Name</span></span>
<span data-ttu-id="349d3-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="349d3-120">WebApp Name</span></span>

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

### <span data-ttu-id="349d3-121">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="349d3-121">-OutputFile</span></span>
<span data-ttu-id="349d3-122">Выходной файл</span><span class="sxs-lookup"><span data-stu-id="349d3-122">Output File</span></span>

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

### <span data-ttu-id="349d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="349d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="349d3-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="349d3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="349d3-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="349d3-125">-Slot</span></span>
<span data-ttu-id="349d3-126">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="349d3-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="349d3-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="349d3-127">-WebApp</span></span>
<span data-ttu-id="349d3-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="349d3-128">WebApp Object</span></span>

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

### <span data-ttu-id="349d3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349d3-129">CommonParameters</span></span>
<span data-ttu-id="349d3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="349d3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349d3-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="349d3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349d3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="349d3-132">INPUTS</span></span>

### <span data-ttu-id="349d3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="349d3-133">System.String</span></span>

### <span data-ttu-id="349d3-134">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="349d3-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="349d3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="349d3-135">OUTPUTS</span></span>

### <span data-ttu-id="349d3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="349d3-136">System.String</span></span>

## <span data-ttu-id="349d3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="349d3-137">NOTES</span></span>

## <span data-ttu-id="349d3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="349d3-138">RELATED LINKS</span></span>

[<span data-ttu-id="349d3-139">Сброс — AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="349d3-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="349d3-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="349d3-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="349d3-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="349d3-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
