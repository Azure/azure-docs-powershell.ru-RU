---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 426fc5c6cac67da7b0380b3a5e5e40cc1b533366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733072"
---
# <span data-ttu-id="2f6a7-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f6a7-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="2f6a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f6a7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f6a7-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f6a7-103">SYNTAX</span></span>

### <span data-ttu-id="2f6a7-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2f6a7-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f6a7-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2f6a7-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f6a7-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f6a7-106">DESCRIPTION</span></span>
<span data-ttu-id="2f6a7-107">Командлет **Get-AzureRmWebAppBackupConfiguration** получает конфигурацию резервного копирования веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2f6a7-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="2f6a7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f6a7-108">EXAMPLES</span></span>

### <span data-ttu-id="2f6a7-109">1:</span><span class="sxs-lookup"><span data-stu-id="2f6a7-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="2f6a7-110">Эта команда получает конфигурацию резервного копирования из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="2f6a7-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2f6a7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f6a7-111">PARAMETERS</span></span>

### <span data-ttu-id="2f6a7-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f6a7-112">-Name</span></span>
<span data-ttu-id="2f6a7-113">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="2f6a7-113">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6a7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f6a7-114">-ResourceGroupName</span></span>
<span data-ttu-id="2f6a7-115">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2f6a7-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6a7-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="2f6a7-116">-Slot</span></span>
<span data-ttu-id="2f6a7-117">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="2f6a7-117">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6a7-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2f6a7-118">-WebApp</span></span>
<span data-ttu-id="2f6a7-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="2f6a7-119">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f6a7-120">-DefaultProfile</span></span>
<span data-ttu-id="2f6a7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f6a7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f6a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6a7-122">CommonParameters</span></span>
<span data-ttu-id="2f6a7-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f6a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f6a7-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f6a7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6a7-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f6a7-125">INPUTS</span></span>

### <span data-ttu-id="2f6a7-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="2f6a7-126">Site</span></span>
<span data-ttu-id="2f6a7-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2f6a7-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2f6a7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f6a7-128">OUTPUTS</span></span>

### <span data-ttu-id="2f6a7-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f6a7-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="2f6a7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f6a7-130">NOTES</span></span>

## <span data-ttu-id="2f6a7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f6a7-131">RELATED LINKS</span></span>

