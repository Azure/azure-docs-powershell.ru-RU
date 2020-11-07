---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 81c9d87ecd93097c7e114a312b68d25d7dd681c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732086"
---
# <span data-ttu-id="55861-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="55861-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="55861-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55861-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55861-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55861-103">SYNTAX</span></span>

### <span data-ttu-id="55861-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="55861-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55861-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="55861-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55861-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55861-106">DESCRIPTION</span></span>
<span data-ttu-id="55861-107">Командлет **Get-AzureRmWebAppBackupConfiguration** получает конфигурацию резервного копирования веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="55861-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="55861-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55861-108">EXAMPLES</span></span>

### <span data-ttu-id="55861-109">1:</span><span class="sxs-lookup"><span data-stu-id="55861-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="55861-110">Эта команда получает конфигурацию резервного копирования из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="55861-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="55861-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55861-111">PARAMETERS</span></span>

### <span data-ttu-id="55861-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55861-112">-DefaultProfile</span></span>
<span data-ttu-id="55861-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55861-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55861-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55861-114">-Name</span></span>
<span data-ttu-id="55861-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="55861-115">WebApp Name</span></span>

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

### <span data-ttu-id="55861-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55861-116">-ResourceGroupName</span></span>
<span data-ttu-id="55861-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="55861-117">Resource Group Name</span></span>

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

### <span data-ttu-id="55861-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="55861-118">-Slot</span></span>
<span data-ttu-id="55861-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="55861-119">Slot Name</span></span>

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

### <span data-ttu-id="55861-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="55861-120">-WebApp</span></span>
<span data-ttu-id="55861-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="55861-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55861-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55861-122">CommonParameters</span></span>
<span data-ttu-id="55861-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55861-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55861-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55861-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55861-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55861-125">INPUTS</span></span>

### <span data-ttu-id="55861-126">System. String</span><span class="sxs-lookup"><span data-stu-id="55861-126">System.String</span></span>

### <span data-ttu-id="55861-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="55861-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="55861-128">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="55861-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="55861-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55861-129">OUTPUTS</span></span>

### <span data-ttu-id="55861-130">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="55861-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="55861-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="55861-131">NOTES</span></span>

## <span data-ttu-id="55861-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55861-132">RELATED LINKS</span></span>
