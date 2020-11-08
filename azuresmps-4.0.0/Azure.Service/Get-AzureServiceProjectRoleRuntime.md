---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075598"
---
# <span data-ttu-id="10dc6-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="10dc6-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="10dc6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="10dc6-103">Получение сред выполнения, доступных для установки в роли.</span><span class="sxs-lookup"><span data-stu-id="10dc6-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="10dc6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10dc6-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10dc6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10dc6-105">DESCRIPTION</span></span>
<span data-ttu-id="10dc6-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10dc6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="10dc6-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="10dc6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="10dc6-108">Возвращает среды выполнения, доступные для установки в роли.</span><span class="sxs-lookup"><span data-stu-id="10dc6-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="10dc6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10dc6-109">EXAMPLES</span></span>

## <span data-ttu-id="10dc6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10dc6-110">PARAMETERS</span></span>

### <span data-ttu-id="10dc6-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="10dc6-111">-Profile</span></span>
<span data-ttu-id="10dc6-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10dc6-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10dc6-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10dc6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10dc6-114">-Runtime</span><span class="sxs-lookup"><span data-stu-id="10dc6-114">-Runtime</span></span>
<span data-ttu-id="10dc6-115">Имя среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="10dc6-115">The name of the runtime.</span></span>
<span data-ttu-id="10dc6-116">Если указана среда выполнения, будут возвращены только определенные версии этой среды выполнения, доступные для установки в вашей роли в Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="10dc6-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

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

### <span data-ttu-id="10dc6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10dc6-117">CommonParameters</span></span>
<span data-ttu-id="10dc6-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10dc6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10dc6-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10dc6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10dc6-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10dc6-120">INPUTS</span></span>

## <span data-ttu-id="10dc6-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10dc6-121">OUTPUTS</span></span>

## <span data-ttu-id="10dc6-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="10dc6-122">NOTES</span></span>

## <span data-ttu-id="10dc6-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10dc6-123">RELATED LINKS</span></span>

[<span data-ttu-id="10dc6-124">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="10dc6-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="10dc6-125">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="10dc6-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="10dc6-126">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="10dc6-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="10dc6-127">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="10dc6-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


