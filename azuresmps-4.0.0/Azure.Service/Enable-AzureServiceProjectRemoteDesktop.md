---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075683"
---
# <span data-ttu-id="d6fcf-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="d6fcf-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="d6fcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fcf-103">Разрешает удаленному рабочему столу доступ к облачной службе.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="d6fcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6fcf-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d6fcf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="d6fcf-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d6fcf-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d6fcf-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d6fcf-108">Командлет **Enable-AzureServiceProjectRemoteDesktop** позволяет удаленному рабочему столу получать доступ к облачной службе.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="d6fcf-109">Чтобы изменения вступили в силу, необходимо опубликовать службу с помощью командлета **Publish-AzureServiceProject** после включения доступа к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="d6fcf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6fcf-110">EXAMPLES</span></span>

## <span data-ttu-id="d6fcf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6fcf-111">PARAMETERS</span></span>

### <span data-ttu-id="d6fcf-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6fcf-112">-PassThru</span></span>
<span data-ttu-id="d6fcf-113">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6fcf-114">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6fcf-115">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="d6fcf-115">-Password</span></span>
<span data-ttu-id="d6fcf-116">Указывает пароль.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fcf-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="d6fcf-117">-Profile</span></span>
<span data-ttu-id="d6fcf-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6fcf-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6fcf-120">-Username</span><span class="sxs-lookup"><span data-stu-id="d6fcf-120">-Username</span></span>
<span data-ttu-id="d6fcf-121">Указывает имя пользователя, используемое при подключении к экземпляру роли в Azure через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="d6fcf-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fcf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fcf-122">CommonParameters</span></span>
<span data-ttu-id="d6fcf-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6fcf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fcf-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6fcf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fcf-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6fcf-125">INPUTS</span></span>

## <span data-ttu-id="d6fcf-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6fcf-126">OUTPUTS</span></span>

## <span data-ttu-id="d6fcf-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6fcf-127">NOTES</span></span>

## <span data-ttu-id="d6fcf-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6fcf-128">RELATED LINKS</span></span>

[<span data-ttu-id="d6fcf-129">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="d6fcf-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="d6fcf-130">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d6fcf-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


