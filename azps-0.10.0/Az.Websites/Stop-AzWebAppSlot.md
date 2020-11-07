---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 4ac4482cb5972553b1dad3972200d2f0eb032fe4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910550"
---
# <span data-ttu-id="12a00-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="12a00-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="12a00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12a00-102">SYNOPSIS</span></span>
<span data-ttu-id="12a00-103">Останавливает область веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="12a00-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="12a00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12a00-104">SYNTAX</span></span>

### <span data-ttu-id="12a00-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="12a00-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12a00-106">S2</span><span class="sxs-lookup"><span data-stu-id="12a00-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a00-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12a00-107">DESCRIPTION</span></span>
<span data-ttu-id="12a00-108">Командлет **Stop-AzWebAppSlot** останавливает работу с слотом веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="12a00-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="12a00-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12a00-109">EXAMPLES</span></span>

### <span data-ttu-id="12a00-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12a00-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="12a00-111">Эта команда останавливает Slot001 слотов, относящихся к веб-приложению ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="12a00-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="12a00-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12a00-112">PARAMETERS</span></span>

### <span data-ttu-id="12a00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a00-113">-DefaultProfile</span></span>
<span data-ttu-id="12a00-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12a00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12a00-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12a00-115">-Name</span></span>
<span data-ttu-id="12a00-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="12a00-116">WebApp Name</span></span>

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

### <span data-ttu-id="12a00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a00-117">-ResourceGroupName</span></span>
<span data-ttu-id="12a00-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="12a00-118">Resource Group Name</span></span>

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

### <span data-ttu-id="12a00-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="12a00-119">-Slot</span></span>
<span data-ttu-id="12a00-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="12a00-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="12a00-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="12a00-121">-WebApp</span></span>
<span data-ttu-id="12a00-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="12a00-122">WebApp Object</span></span>

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

### <span data-ttu-id="12a00-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a00-123">CommonParameters</span></span>
<span data-ttu-id="12a00-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12a00-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a00-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a00-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a00-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12a00-126">INPUTS</span></span>

### <span data-ttu-id="12a00-127">Семейств</span><span class="sxs-lookup"><span data-stu-id="12a00-127">Site</span></span>
<span data-ttu-id="12a00-128">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="12a00-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="12a00-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12a00-129">OUTPUTS</span></span>

## <span data-ttu-id="12a00-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="12a00-130">NOTES</span></span>

## <span data-ttu-id="12a00-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12a00-131">RELATED LINKS</span></span>

