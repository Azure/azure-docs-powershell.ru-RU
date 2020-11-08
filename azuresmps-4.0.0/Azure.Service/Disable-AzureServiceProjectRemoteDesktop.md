---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075696"
---
# <span data-ttu-id="40d18-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="40d18-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="40d18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40d18-102">SYNOPSIS</span></span>
<span data-ttu-id="40d18-103">Запрещает удаленному рабочему столу доступ к облачной службе.</span><span class="sxs-lookup"><span data-stu-id="40d18-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="40d18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40d18-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="40d18-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d18-105">DESCRIPTION</span></span>
<span data-ttu-id="40d18-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40d18-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="40d18-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="40d18-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="40d18-108">**Disable-AzureServiceProjectRemoteDesktop** отключает удаленный рабочий стол для доступа к размещенной службе.</span><span class="sxs-lookup"><span data-stu-id="40d18-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="40d18-109">Чтобы изменения вступили в силу, необходимо опубликовать службу с помощью командлета **Publish-AzureServiceProject** после отключения доступа к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="40d18-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="40d18-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40d18-110">EXAMPLES</span></span>

## <span data-ttu-id="40d18-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40d18-111">PARAMETERS</span></span>

### <span data-ttu-id="40d18-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40d18-112">-PassThru</span></span>
<span data-ttu-id="40d18-113">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="40d18-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="40d18-114">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="40d18-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="40d18-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="40d18-115">-Profile</span></span>
<span data-ttu-id="40d18-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="40d18-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40d18-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="40d18-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40d18-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d18-118">CommonParameters</span></span>
<span data-ttu-id="40d18-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40d18-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d18-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d18-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d18-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40d18-121">INPUTS</span></span>

## <span data-ttu-id="40d18-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d18-122">OUTPUTS</span></span>

## <span data-ttu-id="40d18-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="40d18-123">NOTES</span></span>

## <span data-ttu-id="40d18-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40d18-124">RELATED LINKS</span></span>

[<span data-ttu-id="40d18-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="40d18-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


