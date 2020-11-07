---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910563"
---
# <span data-ttu-id="5f390-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f390-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="5f390-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f390-102">SYNOPSIS</span></span>
<span data-ttu-id="5f390-103">Запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="5f390-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="5f390-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f390-104">SYNTAX</span></span>

### <span data-ttu-id="5f390-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="5f390-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f390-106">S2</span><span class="sxs-lookup"><span data-stu-id="5f390-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f390-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f390-107">DESCRIPTION</span></span>
<span data-ttu-id="5f390-108">Командлет **Start-AzWebAppSlot** запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="5f390-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="5f390-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f390-109">EXAMPLES</span></span>

### <span data-ttu-id="5f390-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f390-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="5f390-111">Эта команда запускает ячейку с именем Slot001, относящуюся к веб-приложению ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5f390-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="5f390-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f390-112">PARAMETERS</span></span>

### <span data-ttu-id="5f390-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f390-113">-DefaultProfile</span></span>
<span data-ttu-id="5f390-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f390-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f390-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f390-115">-Name</span></span>
<span data-ttu-id="5f390-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="5f390-116">WebApp Name</span></span>

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

### <span data-ttu-id="5f390-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f390-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f390-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5f390-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5f390-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="5f390-119">-Slot</span></span>
<span data-ttu-id="5f390-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="5f390-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5f390-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5f390-121">-WebApp</span></span>
<span data-ttu-id="5f390-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="5f390-122">WebApp Object</span></span>

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

### <span data-ttu-id="5f390-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f390-123">CommonParameters</span></span>
<span data-ttu-id="5f390-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f390-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f390-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f390-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f390-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f390-126">INPUTS</span></span>

### <span data-ttu-id="5f390-127">Семейств</span><span class="sxs-lookup"><span data-stu-id="5f390-127">Site</span></span>
<span data-ttu-id="5f390-128">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5f390-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5f390-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f390-129">OUTPUTS</span></span>

## <span data-ttu-id="5f390-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f390-130">NOTES</span></span>

## <span data-ttu-id="5f390-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f390-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f390-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f390-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="5f390-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f390-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="5f390-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f390-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="5f390-135">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f390-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="5f390-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f390-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="5f390-137">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f390-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="5f390-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5f390-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
