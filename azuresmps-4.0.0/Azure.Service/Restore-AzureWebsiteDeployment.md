---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075463"
---
# <span data-ttu-id="e254e-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="e254e-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="e254e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e254e-102">SYNOPSIS</span></span>
<span data-ttu-id="e254e-103">Повторное развертывание предыдущего развертывания веб-сайта в Azure.</span><span class="sxs-lookup"><span data-stu-id="e254e-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="e254e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e254e-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e254e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e254e-105">DESCRIPTION</span></span>
<span data-ttu-id="e254e-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e254e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e254e-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e254e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e254e-108">Командлет **redeploy-AzureWebsiteDeployment** повторно развертывает предыдущее развертывание веб-сайта в Azure.</span><span class="sxs-lookup"><span data-stu-id="e254e-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="e254e-109">Этот процесс заменяет текущее развертывание выбранным развертыванием.</span><span class="sxs-lookup"><span data-stu-id="e254e-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="e254e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e254e-110">EXAMPLES</span></span>

### <span data-ttu-id="e254e-111">Пример 1: повторное развертывание сайта</span><span class="sxs-lookup"><span data-stu-id="e254e-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="e254e-112">Эта команда повторно разворачивает развертывание с ИД f876543210 для веб-сайта с именем ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="e254e-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="e254e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e254e-113">PARAMETERS</span></span>

### <span data-ttu-id="e254e-114">-CommitId</span><span class="sxs-lookup"><span data-stu-id="e254e-114">-CommitId</span></span>
<span data-ttu-id="e254e-115">Указывает идентификатор развертывания, который нужно повторно развернуть.</span><span class="sxs-lookup"><span data-stu-id="e254e-115">Specifies the identifier of the deployment to redeploy.</span></span>

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

### <span data-ttu-id="e254e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e254e-116">-Force</span></span>
<span data-ttu-id="e254e-117">Если включено, повторно развертывается предыдущее развертывание без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e254e-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e254e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e254e-118">-Name</span></span>
<span data-ttu-id="e254e-119">Указывает имя веб-сайта, который нужно повторно развернуть.</span><span class="sxs-lookup"><span data-stu-id="e254e-119">Specifies the name of the website to redeploy.</span></span>

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

### <span data-ttu-id="e254e-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="e254e-120">-Profile</span></span>
<span data-ttu-id="e254e-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e254e-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e254e-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e254e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e254e-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="e254e-123">-Slot</span></span>
<span data-ttu-id="e254e-124">Указывает имя гнезда.</span><span class="sxs-lookup"><span data-stu-id="e254e-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="e254e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e254e-125">-Confirm</span></span>
<span data-ttu-id="e254e-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e254e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e254e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e254e-127">-WhatIf</span></span>
<span data-ttu-id="e254e-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e254e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e254e-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e254e-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e254e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e254e-130">CommonParameters</span></span>
<span data-ttu-id="e254e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e254e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e254e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e254e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e254e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e254e-133">INPUTS</span></span>

## <span data-ttu-id="e254e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e254e-134">OUTPUTS</span></span>

## <span data-ttu-id="e254e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e254e-135">NOTES</span></span>

## <span data-ttu-id="e254e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e254e-136">RELATED LINKS</span></span>

[<span data-ttu-id="e254e-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e254e-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="e254e-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="e254e-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


