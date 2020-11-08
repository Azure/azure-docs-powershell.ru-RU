---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076509"
---
# <span data-ttu-id="e7031-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="e7031-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="e7031-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7031-102">SYNOPSIS</span></span>
<span data-ttu-id="e7031-103">Возвращает развертывание для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="e7031-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="e7031-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7031-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7031-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7031-105">DESCRIPTION</span></span>
<span data-ttu-id="e7031-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7031-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e7031-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e7031-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e7031-108">Получает развертывания для веб-сайта в Azure.</span><span class="sxs-lookup"><span data-stu-id="e7031-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="e7031-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7031-109">EXAMPLES</span></span>

## <span data-ttu-id="e7031-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7031-110">PARAMETERS</span></span>

### <span data-ttu-id="e7031-111">-CommitId</span><span class="sxs-lookup"><span data-stu-id="e7031-111">-CommitId</span></span>
<span data-ttu-id="e7031-112">Указывает уникальный идентификатор для развертывания.</span><span class="sxs-lookup"><span data-stu-id="e7031-112">Specifies the unique ID for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7031-113">-Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="e7031-113">-Details</span></span>
<span data-ttu-id="e7031-114">Отображаются подробные сведения о развертываниях.</span><span class="sxs-lookup"><span data-stu-id="e7031-114">Shows detailed information about the deployments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7031-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="e7031-115">-MaxResults</span></span>
<span data-ttu-id="e7031-116">Указывает наибольшее число результатов, возвращаемых командой.</span><span class="sxs-lookup"><span data-stu-id="e7031-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7031-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7031-117">-Name</span></span>
<span data-ttu-id="e7031-118">Указывает имя веб-сайта, сведения о развертывании которого требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e7031-118">Specifies the name of the website for which you want to get deployment information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7031-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="e7031-119">-Profile</span></span>
<span data-ttu-id="e7031-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e7031-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7031-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7031-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7031-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="e7031-122">-Slot</span></span>
<span data-ttu-id="e7031-123">Указывает имя гнезда.</span><span class="sxs-lookup"><span data-stu-id="e7031-123">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7031-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7031-124">CommonParameters</span></span>
<span data-ttu-id="e7031-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7031-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7031-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7031-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7031-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7031-127">INPUTS</span></span>

## <span data-ttu-id="e7031-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7031-128">OUTPUTS</span></span>

## <span data-ttu-id="e7031-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7031-129">NOTES</span></span>

## <span data-ttu-id="e7031-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7031-130">RELATED LINKS</span></span>

[<span data-ttu-id="e7031-131">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="e7031-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


