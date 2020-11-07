---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4c6dc810d35feedd0d0d43e0bd3b3efb7c9b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910623"
---
# <span data-ttu-id="5b235-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b235-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5b235-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b235-102">SYNOPSIS</span></span>

## <span data-ttu-id="5b235-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b235-103">SYNTAX</span></span>

### <span data-ttu-id="5b235-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5b235-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b235-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5b235-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b235-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b235-106">DESCRIPTION</span></span>
<span data-ttu-id="5b235-107">Командлет **Get-AzWebAppBackupConfiguration** получает конфигурацию резервного копирования веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="5b235-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="5b235-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b235-108">EXAMPLES</span></span>

### <span data-ttu-id="5b235-109">1:</span><span class="sxs-lookup"><span data-stu-id="5b235-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="5b235-110">Эта команда получает конфигурацию резервного копирования из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5b235-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5b235-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b235-111">PARAMETERS</span></span>

### <span data-ttu-id="5b235-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b235-112">-DefaultProfile</span></span>
<span data-ttu-id="5b235-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b235-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b235-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b235-114">-Name</span></span>
<span data-ttu-id="5b235-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="5b235-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b235-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b235-116">-ResourceGroupName</span></span>
<span data-ttu-id="5b235-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5b235-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b235-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="5b235-118">-Slot</span></span>
<span data-ttu-id="5b235-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="5b235-119">Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b235-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5b235-120">-WebApp</span></span>
<span data-ttu-id="5b235-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="5b235-121">WebApp Name</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b235-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b235-122">CommonParameters</span></span>
<span data-ttu-id="5b235-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b235-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b235-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b235-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b235-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b235-125">INPUTS</span></span>

### <span data-ttu-id="5b235-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="5b235-126">Site</span></span>
<span data-ttu-id="5b235-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5b235-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5b235-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b235-128">OUTPUTS</span></span>

### <span data-ttu-id="5b235-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b235-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5b235-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b235-130">NOTES</span></span>

## <span data-ttu-id="5b235-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b235-131">RELATED LINKS</span></span>

