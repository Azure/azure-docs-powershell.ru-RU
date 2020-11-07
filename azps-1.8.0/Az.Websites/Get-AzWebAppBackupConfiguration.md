---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 3c48c913223d8122e7b26fe0e95db06f0e973ad1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728365"
---
# <span data-ttu-id="f0d79-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0d79-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f0d79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0d79-102">SYNOPSIS</span></span>

## <span data-ttu-id="f0d79-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0d79-103">SYNTAX</span></span>

### <span data-ttu-id="f0d79-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f0d79-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0d79-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f0d79-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0d79-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0d79-106">DESCRIPTION</span></span>
<span data-ttu-id="f0d79-107">Командлет **Get-AzWebAppBackupConfiguration** получает конфигурацию резервного копирования веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d79-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="f0d79-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0d79-108">EXAMPLES</span></span>

### <span data-ttu-id="f0d79-109">1:</span><span class="sxs-lookup"><span data-stu-id="f0d79-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="f0d79-110">Эта команда получает конфигурацию резервного копирования из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="f0d79-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f0d79-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0d79-111">PARAMETERS</span></span>

### <span data-ttu-id="f0d79-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d79-112">-DefaultProfile</span></span>
<span data-ttu-id="f0d79-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d79-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d79-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0d79-114">-Name</span></span>
<span data-ttu-id="f0d79-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="f0d79-115">WebApp Name</span></span>

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

### <span data-ttu-id="f0d79-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d79-116">-ResourceGroupName</span></span>
<span data-ttu-id="f0d79-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0d79-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f0d79-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="f0d79-118">-Slot</span></span>
<span data-ttu-id="f0d79-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="f0d79-119">Slot Name</span></span>

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

### <span data-ttu-id="f0d79-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f0d79-120">-WebApp</span></span>
<span data-ttu-id="f0d79-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="f0d79-121">WebApp Name</span></span>

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

### <span data-ttu-id="f0d79-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d79-122">CommonParameters</span></span>
<span data-ttu-id="f0d79-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0d79-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d79-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d79-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d79-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0d79-125">INPUTS</span></span>

### <span data-ttu-id="f0d79-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d79-126">System.String</span></span>

### <span data-ttu-id="f0d79-127">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="f0d79-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f0d79-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0d79-128">OUTPUTS</span></span>

### <span data-ttu-id="f0d79-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0d79-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f0d79-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0d79-130">NOTES</span></span>

## <span data-ttu-id="f0d79-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0d79-131">RELATED LINKS</span></span>
