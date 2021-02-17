---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232716"
---
# <span data-ttu-id="1faf2-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1faf2-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="1faf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1faf2-102">SYNOPSIS</span></span>
<span data-ttu-id="1faf2-103">Удалите имена сертификатов или их тем, используемых для проверки подлинности клиента на кластере.</span><span class="sxs-lookup"><span data-stu-id="1faf2-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="1faf2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1faf2-104">SYNTAX</span></span>

### <span data-ttu-id="1faf2-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="1faf2-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1faf2-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="1faf2-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faf2-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="1faf2-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faf2-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="1faf2-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1faf2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1faf2-109">DESCRIPTION</span></span>
<span data-ttu-id="1faf2-110">Используйте **Remove-AzServiceFabricClientCertificate,** чтобы удалить сертификаты клиентов или имена их субъектов, которые используются для проверки подлинности клиента на кластере.</span><span class="sxs-lookup"><span data-stu-id="1faf2-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="1faf2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1faf2-111">EXAMPLES</span></span>

### <span data-ttu-id="1faf2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1faf2-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="1faf2-113">Эта команда удаляет из кластера сертификат клиента с препечаткой 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A.</span><span class="sxs-lookup"><span data-stu-id="1faf2-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="1faf2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1faf2-114">PARAMETERS</span></span>

### <span data-ttu-id="1faf2-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="1faf2-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="1faf2-116">Эскиз "Указание сертификата клиента" с разрешением администратора</span><span class="sxs-lookup"><span data-stu-id="1faf2-116">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="1faf2-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="1faf2-118">Указание общего имени клиента, препечатки выдачи и типа проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="1faf2-118">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="1faf2-119">-CommonName</span></span>
<span data-ttu-id="1faf2-120">Указание общего имени сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="1faf2-120">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1faf2-121">-DefaultProfile</span></span>
<span data-ttu-id="1faf2-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1faf2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1faf2-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="1faf2-123">-IssuerThumbprint</span></span>
<span data-ttu-id="1faf2-124">Указание thumbprint of client certificate's issuer</span><span class="sxs-lookup"><span data-stu-id="1faf2-124">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1faf2-125">-Name</span></span>
<span data-ttu-id="1faf2-126">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="1faf2-126">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="1faf2-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="1faf2-128">Укажите эскиз сертификата клиента с разрешением только на чтение</span><span class="sxs-lookup"><span data-stu-id="1faf2-128">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1faf2-129">-ResourceGroupName</span></span>
<span data-ttu-id="1faf2-130">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1faf2-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-131">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="1faf2-131">-Thumbprint</span></span>
<span data-ttu-id="1faf2-132">Укажите эскиз сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="1faf2-132">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1faf2-133">-Confirm</span></span>
<span data-ttu-id="1faf2-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1faf2-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1faf2-135">-WhatIf</span></span>
<span data-ttu-id="1faf2-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1faf2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1faf2-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1faf2-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1faf2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1faf2-138">CommonParameters</span></span>
<span data-ttu-id="1faf2-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1faf2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1faf2-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1faf2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1faf2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1faf2-141">INPUTS</span></span>

### <span data-ttu-id="1faf2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1faf2-142">System.String</span></span>

### <span data-ttu-id="1faf2-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1faf2-143">System.String[]</span></span>

### <span data-ttu-id="1faf2-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="1faf2-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="1faf2-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1faf2-145">OUTPUTS</span></span>

### <span data-ttu-id="1faf2-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="1faf2-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1faf2-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1faf2-147">NOTES</span></span>

## <span data-ttu-id="1faf2-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1faf2-148">RELATED LINKS</span></span>

[<span data-ttu-id="1faf2-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1faf2-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
