---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910569"
---
# <span data-ttu-id="ab515-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab515-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="ab515-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab515-102">SYNOPSIS</span></span>

## <span data-ttu-id="ab515-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab515-103">SYNTAX</span></span>

### <span data-ttu-id="ab515-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="ab515-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab515-105">S2</span><span class="sxs-lookup"><span data-stu-id="ab515-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab515-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab515-106">DESCRIPTION</span></span>
<span data-ttu-id="ab515-107">Командлет **restarting-AzWebAppSlot** останавливается, а затем запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="ab515-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="ab515-108">Если ячейка веб-приложения находится в остановленном состоянии, используйте командлет Start-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="ab515-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="ab515-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab515-109">EXAMPLES</span></span>

### <span data-ttu-id="ab515-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab515-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="ab515-111">Эта команда перезапускает слот Slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="ab515-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ab515-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab515-112">PARAMETERS</span></span>

### <span data-ttu-id="ab515-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab515-113">-DefaultProfile</span></span>
<span data-ttu-id="ab515-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab515-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab515-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ab515-115">-Name</span></span>
<span data-ttu-id="ab515-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ab515-116">WebApp Name</span></span>

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

### <span data-ttu-id="ab515-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab515-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab515-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ab515-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ab515-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="ab515-119">-Slot</span></span>
<span data-ttu-id="ab515-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="ab515-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ab515-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ab515-121">-WebApp</span></span>
<span data-ttu-id="ab515-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="ab515-122">WebApp Object</span></span>

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

### <span data-ttu-id="ab515-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab515-123">CommonParameters</span></span>
<span data-ttu-id="ab515-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab515-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab515-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab515-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab515-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab515-126">INPUTS</span></span>

### <span data-ttu-id="ab515-127">Семейств</span><span class="sxs-lookup"><span data-stu-id="ab515-127">Site</span></span>
<span data-ttu-id="ab515-128">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ab515-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ab515-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab515-129">OUTPUTS</span></span>

## <span data-ttu-id="ab515-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab515-130">NOTES</span></span>

## <span data-ttu-id="ab515-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab515-131">RELATED LINKS</span></span>

[<span data-ttu-id="ab515-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab515-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="ab515-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab515-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="ab515-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab515-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="ab515-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab515-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="ab515-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab515-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="ab515-137">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab515-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="ab515-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab515-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
