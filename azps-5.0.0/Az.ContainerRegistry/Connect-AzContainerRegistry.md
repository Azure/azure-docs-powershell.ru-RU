---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245590"
---
# <span data-ttu-id="5f003-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5f003-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="5f003-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f003-102">SYNOPSIS</span></span>
<span data-ttu-id="5f003-103">Войдите в реестр контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="5f003-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="5f003-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f003-104">SYNTAX</span></span>

### <span data-ttu-id="5f003-105">WithoutNameAndPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f003-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f003-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f003-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f003-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f003-107">DESCRIPTION</span></span>
<span data-ttu-id="5f003-108">Войдите в реестр контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="5f003-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="5f003-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f003-109">EXAMPLES</span></span>

### <span data-ttu-id="5f003-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f003-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="5f003-111">Войдите в службу контроля учетных записей без учетных данных, если у вас уже есть вход в службу Azure.</span><span class="sxs-lookup"><span data-stu-id="5f003-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="5f003-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5f003-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="5f003-113">Вход в учетную запись контроля учетных записей с именем пользователя и паролем администратора при включении администратора.</span><span class="sxs-lookup"><span data-stu-id="5f003-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="5f003-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5f003-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="5f003-115">Войдите в систему контроля доступа с помощью идентификатора и пароля основного приложения-службы.</span><span class="sxs-lookup"><span data-stu-id="5f003-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="5f003-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f003-116">PARAMETERS</span></span>

### <span data-ttu-id="5f003-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f003-117">-DefaultProfile</span></span>
<span data-ttu-id="5f003-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f003-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f003-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f003-119">-Name</span></span>
<span data-ttu-id="5f003-120">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="5f003-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f003-121">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="5f003-121">-Password</span></span>
<span data-ttu-id="5f003-122">Пароль для контейнера реестра Azure.</span><span class="sxs-lookup"><span data-stu-id="5f003-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f003-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="5f003-123">-UserName</span></span>
<span data-ttu-id="5f003-124">Имя пользователя в реестре контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="5f003-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f003-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f003-125">CommonParameters</span></span>
<span data-ttu-id="5f003-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f003-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f003-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f003-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f003-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f003-128">INPUTS</span></span>

### <span data-ttu-id="5f003-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5f003-129">System.String</span></span>

## <span data-ttu-id="5f003-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f003-130">OUTPUTS</span></span>

### <span data-ttu-id="5f003-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f003-131">System.Boolean</span></span>

## <span data-ttu-id="5f003-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f003-132">NOTES</span></span>

## <span data-ttu-id="5f003-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f003-133">RELATED LINKS</span></span>
