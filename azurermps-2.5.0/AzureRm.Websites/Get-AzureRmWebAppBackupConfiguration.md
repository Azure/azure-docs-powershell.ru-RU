---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 67bf9eb23318e4771c00760d18a5659526c5f45a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913536"
---
# <span data-ttu-id="d672a-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d672a-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d672a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d672a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d672a-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d672a-103">SYNTAX</span></span>

### <span data-ttu-id="d672a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d672a-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d672a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d672a-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d672a-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d672a-106">DESCRIPTION</span></span>
<span data-ttu-id="d672a-107">Командлет **Get-AzureRmWebAppBackupConfiguration** получает конфигурацию резервного копирования веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d672a-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="d672a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d672a-108">EXAMPLES</span></span>

### <span data-ttu-id="d672a-109">1:</span><span class="sxs-lookup"><span data-stu-id="d672a-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="d672a-110">Эта команда получает конфигурацию резервного копирования из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d672a-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d672a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d672a-111">PARAMETERS</span></span>

### <span data-ttu-id="d672a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d672a-112">-DefaultProfile</span></span>
<span data-ttu-id="d672a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d672a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d672a-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d672a-114">-Name</span></span>
<span data-ttu-id="d672a-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="d672a-115">WebApp Name</span></span>

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

### <span data-ttu-id="d672a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d672a-116">-ResourceGroupName</span></span>
<span data-ttu-id="d672a-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d672a-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d672a-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="d672a-118">-Slot</span></span>
<span data-ttu-id="d672a-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="d672a-119">Slot Name</span></span>

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

### <span data-ttu-id="d672a-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d672a-120">-WebApp</span></span>
<span data-ttu-id="d672a-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="d672a-121">WebApp Name</span></span>

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

### <span data-ttu-id="d672a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d672a-122">CommonParameters</span></span>
<span data-ttu-id="d672a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d672a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d672a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d672a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d672a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d672a-125">INPUTS</span></span>

### <span data-ttu-id="d672a-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="d672a-126">Site</span></span>
<span data-ttu-id="d672a-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d672a-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d672a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d672a-128">OUTPUTS</span></span>

### <span data-ttu-id="d672a-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d672a-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d672a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d672a-130">NOTES</span></span>

## <span data-ttu-id="d672a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d672a-131">RELATED LINKS</span></span>

