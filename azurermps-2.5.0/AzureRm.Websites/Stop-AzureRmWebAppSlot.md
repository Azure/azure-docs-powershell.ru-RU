---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914318"
---
# <span data-ttu-id="51183-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="51183-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="51183-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51183-102">SYNOPSIS</span></span>
<span data-ttu-id="51183-103">Останавливает область веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="51183-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51183-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51183-104">SYNTAX</span></span>

### <span data-ttu-id="51183-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="51183-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51183-106">S2</span><span class="sxs-lookup"><span data-stu-id="51183-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51183-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51183-107">DESCRIPTION</span></span>
<span data-ttu-id="51183-108">Командлет **Stop-AzureRmWebAppSlot** останавливает работу с слотом веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="51183-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="51183-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51183-109">EXAMPLES</span></span>

### <span data-ttu-id="51183-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="51183-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="51183-111">Эта команда останавливает Slot001 слотов, относящихся к веб-приложению ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="51183-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="51183-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51183-112">PARAMETERS</span></span>

### <span data-ttu-id="51183-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51183-113">-DefaultProfile</span></span>
<span data-ttu-id="51183-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51183-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51183-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51183-115">-Name</span></span>
<span data-ttu-id="51183-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="51183-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51183-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51183-117">-ResourceGroupName</span></span>
<span data-ttu-id="51183-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="51183-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51183-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="51183-119">-Slot</span></span>
<span data-ttu-id="51183-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="51183-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51183-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="51183-121">-WebApp</span></span>
<span data-ttu-id="51183-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="51183-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51183-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51183-123">CommonParameters</span></span>
<span data-ttu-id="51183-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51183-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51183-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51183-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51183-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51183-126">INPUTS</span></span>

### <span data-ttu-id="51183-127">Семейств</span><span class="sxs-lookup"><span data-stu-id="51183-127">Site</span></span>
<span data-ttu-id="51183-128">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="51183-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="51183-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51183-129">OUTPUTS</span></span>

## <span data-ttu-id="51183-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="51183-130">NOTES</span></span>

## <span data-ttu-id="51183-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51183-131">RELATED LINKS</span></span>

