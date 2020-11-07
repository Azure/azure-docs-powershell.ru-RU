---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 02c83e79b5f56d4ef9a6d7730efb5cf5c42a9da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733071"
---
# <span data-ttu-id="1ee04-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="1ee04-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="1ee04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ee04-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ee04-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ee04-103">SYNTAX</span></span>

### <span data-ttu-id="1ee04-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1ee04-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ee04-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1ee04-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ee04-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee04-106">DESCRIPTION</span></span>
<span data-ttu-id="1ee04-107">Командлет **Get-AzureRmWebAppBackupList** получает список резервных копий для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee04-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="1ee04-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ee04-108">EXAMPLES</span></span>

### <span data-ttu-id="1ee04-109">1:</span><span class="sxs-lookup"><span data-stu-id="1ee04-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="1ee04-110">Эта команда возвращает список резервных копий, относящийся к WebApp WebAppStandard, связанному с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ee04-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="1ee04-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ee04-111">PARAMETERS</span></span>

### <span data-ttu-id="1ee04-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ee04-112">-Name</span></span>
<span data-ttu-id="1ee04-113">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="1ee04-113">WebApp Name</span></span>

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

### <span data-ttu-id="1ee04-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ee04-114">-ResourceGroupName</span></span>
<span data-ttu-id="1ee04-115">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1ee04-115">Resource Group Name</span></span>

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

### <span data-ttu-id="1ee04-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="1ee04-116">-Slot</span></span>
<span data-ttu-id="1ee04-117">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="1ee04-117">Slot name</span></span>

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

### <span data-ttu-id="1ee04-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1ee04-118">-WebApp</span></span>
<span data-ttu-id="1ee04-119">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="1ee04-119">Piped WebApp</span></span>

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

### <span data-ttu-id="1ee04-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee04-120">-DefaultProfile</span></span>
<span data-ttu-id="1ee04-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee04-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ee04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee04-122">CommonParameters</span></span>
<span data-ttu-id="1ee04-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ee04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee04-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee04-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee04-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ee04-125">INPUTS</span></span>

### <span data-ttu-id="1ee04-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="1ee04-126">Site</span></span>
<span data-ttu-id="1ee04-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1ee04-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1ee04-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee04-128">OUTPUTS</span></span>

### <span data-ttu-id="1ee04-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="1ee04-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="1ee04-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ee04-130">NOTES</span></span>

## <span data-ttu-id="1ee04-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ee04-131">RELATED LINKS</span></span>

