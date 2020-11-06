---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 91a8c53bc8600006a3a57a5dfefb1141652ca3d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557667"
---
# <span data-ttu-id="2b12e-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b12e-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="2b12e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b12e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b12e-103">Останавливает область веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2b12e-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b12e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b12e-104">SYNTAX</span></span>

### <span data-ttu-id="2b12e-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="2b12e-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b12e-106">S2</span><span class="sxs-lookup"><span data-stu-id="2b12e-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b12e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b12e-107">DESCRIPTION</span></span>
<span data-ttu-id="2b12e-108">Командлет **Stop-AzureRmWebAppSlot** останавливает работу с слотом веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2b12e-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="2b12e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b12e-109">EXAMPLES</span></span>

### <span data-ttu-id="2b12e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b12e-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="2b12e-111">Эта команда останавливает Slot001 слотов, относящихся к веб-приложению ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="2b12e-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2b12e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b12e-112">PARAMETERS</span></span>

### <span data-ttu-id="2b12e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b12e-113">-Name</span></span>
<span data-ttu-id="2b12e-114">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="2b12e-114">WebApp Name</span></span>

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

### <span data-ttu-id="2b12e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b12e-115">-ResourceGroupName</span></span>
<span data-ttu-id="2b12e-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2b12e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="2b12e-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="2b12e-117">-Slot</span></span>
<span data-ttu-id="2b12e-118">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="2b12e-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2b12e-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2b12e-119">-WebApp</span></span>
<span data-ttu-id="2b12e-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="2b12e-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b12e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b12e-121">-DefaultProfile</span></span>
<span data-ttu-id="2b12e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b12e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b12e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b12e-123">CommonParameters</span></span>
<span data-ttu-id="2b12e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b12e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b12e-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b12e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b12e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b12e-126">INPUTS</span></span>

### <span data-ttu-id="2b12e-127">Семейств</span><span class="sxs-lookup"><span data-stu-id="2b12e-127">Site</span></span>
<span data-ttu-id="2b12e-128">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2b12e-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2b12e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b12e-129">OUTPUTS</span></span>

## <span data-ttu-id="2b12e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b12e-130">NOTES</span></span>

## <span data-ttu-id="2b12e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b12e-131">RELATED LINKS</span></span>

