---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913534"
---
# <span data-ttu-id="eb83c-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="eb83c-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="eb83c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb83c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb83c-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb83c-103">SYNTAX</span></span>

### <span data-ttu-id="eb83c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="eb83c-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb83c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="eb83c-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb83c-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb83c-106">DESCRIPTION</span></span>
<span data-ttu-id="eb83c-107">Командлет **Get-AzureRmWebAppBackupList** получает список резервных копий для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="eb83c-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="eb83c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb83c-108">EXAMPLES</span></span>

### <span data-ttu-id="eb83c-109">1:</span><span class="sxs-lookup"><span data-stu-id="eb83c-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="eb83c-110">Эта команда возвращает список резервных копий, относящийся к WebApp WebAppStandard, связанному с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eb83c-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="eb83c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb83c-111">PARAMETERS</span></span>

### <span data-ttu-id="eb83c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb83c-112">-DefaultProfile</span></span>
<span data-ttu-id="eb83c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb83c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb83c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb83c-114">-Name</span></span>
<span data-ttu-id="eb83c-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="eb83c-115">WebApp Name</span></span>

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

### <span data-ttu-id="eb83c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb83c-116">-ResourceGroupName</span></span>
<span data-ttu-id="eb83c-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eb83c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="eb83c-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="eb83c-118">-Slot</span></span>
<span data-ttu-id="eb83c-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="eb83c-119">Slot name</span></span>

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

### <span data-ttu-id="eb83c-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="eb83c-120">-WebApp</span></span>
<span data-ttu-id="eb83c-121">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="eb83c-121">Piped WebApp</span></span>

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

### <span data-ttu-id="eb83c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb83c-122">CommonParameters</span></span>
<span data-ttu-id="eb83c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb83c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb83c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb83c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb83c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb83c-125">INPUTS</span></span>

### <span data-ttu-id="eb83c-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="eb83c-126">Site</span></span>
<span data-ttu-id="eb83c-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eb83c-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eb83c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb83c-128">OUTPUTS</span></span>

### <span data-ttu-id="eb83c-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="eb83c-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="eb83c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb83c-130">NOTES</span></span>

## <span data-ttu-id="eb83c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb83c-131">RELATED LINKS</span></span>

